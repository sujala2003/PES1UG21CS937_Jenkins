pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    sh 'g++ -o PES1UG21CS937 PES1UG21CS937-1.cpp'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using shell script
                    sh './PES1UG21CS937'
                }
            }
        }
        stage('Deploy') {
            steps {
                // Add deployment steps here
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

