pipeline {
    agent any

    stages {
        stage('Build App') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                sh 'npm install'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t prod-microservice:ci .'
            }
        }
    }
}
