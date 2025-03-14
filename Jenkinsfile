pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile .cpp file
                    sh 'g++ hello.cpp -o hello.out'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of the compiled .cpp file
                    sh './hello.out'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
