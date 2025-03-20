pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'g++ main/hello.cpp -o main/hello_exec'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './main/hello_exec'
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
            echo 'Pipeline failed!'
        }
    }
}
