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
          docker.image('golang:latest').inside {
            dir('src/github.com/trayio') {
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
