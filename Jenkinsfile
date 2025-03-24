pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                
                sh 'this is test'
            }
        }
        stage('Test') {
            steps {
                
                sh 'this is test'
            }
        }
        stage('Deploy') {
            steps {
                
                sh 'echo This is deploy'
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