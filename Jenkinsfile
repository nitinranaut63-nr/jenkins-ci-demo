
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
                sh 'chmod +x app.sh'
                sh 'echo "Building application..."'
            }
        }

        stage('Test') {
            steps {
                sh './app.sh'
            }
        }
    }

    post {
        success {
            echo 'CI pipeline completed successfully!'
        }
        failure {
            echo 'CI pipeline failed. Check the logs.'
        }
    }
}
