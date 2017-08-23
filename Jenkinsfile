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
        DOCKER_REGISTRY = credentials('cdda9cef-e64f-48e5-94ef-fe7ac34c2159')
      }
      
      steps {
        sh 'echo ${DOCKER_REGISTRY}'
      }
    }
  }
}
