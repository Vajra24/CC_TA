pipeline {
    agent any

  stage('Build') {
    steps {
        script {
            // Intentional error: non-existent file
            sh 'g++ non_existent_file.cpp -o hello.out'
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
