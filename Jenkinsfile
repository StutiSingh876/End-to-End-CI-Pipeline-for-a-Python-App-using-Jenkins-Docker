pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-python-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm ci-python-app'
            }
        }
    }
}
