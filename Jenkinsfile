pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('test') {
      steps {
        script {
          docker.image('golang:latest').inside('-v $(pwd):/go/src/github.com/trayio/doorman') {
            sh 'pwd'
            sh 'ls'
            sh 'env'
          }
        }
      }
    }
  }
}
