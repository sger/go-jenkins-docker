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
    stage('Shell script') {
      steps {
        sh 'test.sh'
      }
    }
    stage('Test') {
        steps {
            sh 'go test'
        }
    }
  }
}
