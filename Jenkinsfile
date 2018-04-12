pipeline {
  agent {
    docker 'golang:1.8.0-alpine'
  }
  stages {
    stage('Checkout from GitHub') {
        checkout scm
    }
    stage('Print version') {
      steps {
        sh 'go version'
      }
    }
  }
}