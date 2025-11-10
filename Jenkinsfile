pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/takwaaaaa/jinkins.git'
            }
        }

        stage('Build') {
            steps {
                echo ' Building the application...'
                sh 'echo Build complete!'
            }
        }

        stage('Test') {
            steps {
                echo ' Running tests...'
                sh 'echo All tests passed!'
            }
        }

        stage('Deploy') {
            steps {
                echo ' Deploying the application...'
                sh 'echo Application deployed successfully!'
            }
        }
    }

    post {
        success {
            echo ' Pipeline executed successfully!'
        }
        failure {
            echo ' Pipeline failed!'
        }
    }
}
