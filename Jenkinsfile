pipeline {
    agent any

  stage('Build') {
    steps {
        script {
            // Compile the hello.cpp file into hello.out executable
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
