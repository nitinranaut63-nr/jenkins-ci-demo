
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Source code is available in the workspace'
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building the application..."'
                sh 'cat app.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'test -f app.txt'
                echo 'Application test passed!'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully!'
        }
        failure {
            echo 'CI Pipeline failed. Check the console output.'
        }
    }
}

