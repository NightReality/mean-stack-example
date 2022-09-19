pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/Neha7199/mean-stack-example', branch: 'main')
      }
    }

    stage('Install dependencies') {
      steps {
        sh 'cd client && npm i'
      }
    }

    stage('Build') {
      steps {
        sh 'cd client && npm build'
      }
    }

  }
}