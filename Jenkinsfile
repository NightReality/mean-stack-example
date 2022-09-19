pipeline {
  agent {
    docker {
      image 'node:lts-bullseye-slim'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/NightReality/mean-stack-example', branch: 'main')
      }
    }

    stage('Install dependencies') {
      steps {
        sh 'ls -la'
      }
    }

    stage('Build') {
      steps {
        sh 'cd client && npm build'
      }
    }

  }
}