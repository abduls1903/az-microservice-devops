pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            args '-u root'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build App') {
            steps {
                sh '''
                  node -v
                  npm -v
                  npm install
                '''
            }
        }

        stage('Docker Build') {
            steps {
                sh '''
                  docker build -f Dockerfile.jenkins -t node-app:latest .
                '''
            }
        }
    }
}
