pipeline {
    agent {
        label 'AGENT-2'
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds() // cant run multiple builds at a time
        retry(1)
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
                error 'pipeline failed'
                
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