pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'g++ -o output main.cpp'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'echo "Deployment Complete"'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
