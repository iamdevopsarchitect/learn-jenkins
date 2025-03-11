pipeline {
    agent {
        label 'AGENT-2'
    }
    options{
        timeout(time: 10, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                    sh 'echo This is Build'
                    sh 'sleep 10'
            }
        }
        stage('Test') {
            steps {

                    sh 'echo This is Test'
            }
        }
        stage('Deploy') {
            steps {
                    sh 'echo This is Deploy'
                    //error 'pipeline failed'
            }
        }
    }
    
    post { 
        always { 
            echo 'This section runs always'
            deleteDir()
        }
        success { 
            echo 'This section runs when pipeline success!'
        }
        failure { 
            echo 'This section run when pipeline failure!'
        }
    }
}