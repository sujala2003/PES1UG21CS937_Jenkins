pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script
                    build 'PES1UG21CS937-1'
                    sh 'g++ task5.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of .cpp file using shell script
                    sh './output'
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
