pipeline {
  agent any

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
        sh 'docker build -t myapp:latest .'
      }
    }
  }
}


