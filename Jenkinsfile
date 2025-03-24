pipeline {
    agent {
        label 'AGENT-2'
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds() // cant run multiple builds at a time
        retry(1)
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Build') {
            steps {
                
                sh 'echo this is test'
                sh 'sleep 10'
            }
        }
        stage('Test') {
            steps {
                
                sh 'echo this is test'
            }
        }
        stage('Deploy') {
            steps {
                
                sh 'echo This is deploy'
                //error 'pipeline failed'
                
            }
        }
        stage('Print Params'){
            steps{
                echo "Hello ${params.PERSON}"
                echo "Biography: ${params.BIOGRAPHY}"
                echo "Toggle: ${params.TOGGLE}"
                echo "Choice: ${params.CHOICE}"
                echo "Password: ${params.PASSWORD}"
            }
        }
    }
        post {
        always { 
            echo 'This section runs always'
            deleteDir() // delete build when jenkins pipeline is completed
        }
        success { 
            echo 'This section runs when pipeline success!'
        }
        failure { 
            echo 'This section run when pipeline failure!'
        }
    }
}