pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                    build 'PES1UG21CS937-1'
                    sh 'g++ task5.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                script {
                    sh './output'
                }
            }
            post {
                failure {
                    echo 'Test failed: pipeline failed'
                }
            }
        }
        
        stage('Deploy') {
            steps {
               echo 'deploy'
            }
            post {
                failure {
                    echo 'Deployment failed: pipeline failed'
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
