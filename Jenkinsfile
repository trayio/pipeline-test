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
          ws('go/src/github.com/trayio/testing') {
            docker.image('golang:latest').inside {
              sh 'pwd'
              sh 'ls'
              sh 'env'
            }
          }
        }
      }
    }
  }
}
