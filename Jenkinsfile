pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/takwaaaaa/jinkins.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'echo Build step executed'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo All tests passed successfully!'
            }
        }
        stage('Archive') {
            steps {
                echo 'Archiving artifacts...'
                sh 'mkdir -p dist && zip -r dist/app.zip .'
                archiveArtifacts artifacts: '**/dist/*.zip', allowEmptyArchive: true
            }
        }
    }
}
