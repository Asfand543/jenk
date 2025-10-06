pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('app') {
                    bat 'npm install'
                }
            }
        }
        stage('Test') {
            steps {
                dir('app') {
                    bat 'npm test'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
            }
        }
    }
    post {
        failure {
            echo '❌ Pipeline failed.'
        }
        success {
            echo '✅ Pipeline succeeded.'
        }
    }
}
