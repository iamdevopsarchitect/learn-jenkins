pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                    sh 'echo This is Build'
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
                    error 'pipeline failed'
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