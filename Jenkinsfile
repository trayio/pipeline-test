@Library('Credentials')
import io.tray.Credentials

def x = Credentials.GitHub()

pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('build') {
      environment {
        DOCKER_REGISTRY = "HELLO"
      }
      
      steps {
        script {
          sh 'env'
        }
      }
    }
  }
}
