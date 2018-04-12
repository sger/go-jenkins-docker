pipeline {
  agent {
    docker 'golang:1.9.2-alpine'
  }
  stages {
    stage('Checkout from GitHub') {
        steps {
            checkout scm
        }
    }
    stage('Print version') {
      steps {
        sh 'go version'
      }
    }
    stage('Test') {
        steps {
            sh 'go test'
        }
    }
  }
}