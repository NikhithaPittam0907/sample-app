pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Repository'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t sample-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests'
            }
        }

        stage('Deploy') {
            steps {
                bat 'docker run -d -p 5001:5000 sample-app'
            }
        }
    }
}