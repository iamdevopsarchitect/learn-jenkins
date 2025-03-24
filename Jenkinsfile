pipeline {
    agent {
        label 'AGENT-2'
    }
    stages {
        stage('Build') {
            steps {
                
                sh 'echo this is test'
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
                
            }
        }
    }
        post {
        always { 
            echo 'This section runs always'
            
        }
        success { 
            echo 'This section runs when pipeline success!'
        }
        failure { 
            echo 'This section run when pipeline failure!'
        }
    }
}