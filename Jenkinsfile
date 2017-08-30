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
            sh 'pwd'
            sh 'ls'
            sh 'env'
          }
        }
      }
    }
  }
}
