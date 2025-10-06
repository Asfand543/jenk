pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the project...'
                // Example for Node.js
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example test command
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Example: deploy to folder or copy build files
                bat 'xcopy /E /I dist E:\\deploy-folder'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed.'
        }
    }
}
