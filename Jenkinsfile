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
          customWorkspace '${WORKSPACE}/testing'
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
