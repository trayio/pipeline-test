pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('test') {
      agent {
        docker {
          image 'golang:latest'
          customWorkspace 'go/src/github.com/trayio/testing'
        }
      }

      steps {
        sh 'pwd'
        sh 'ls'
        sh 'env'
      }
    }
  }
}
