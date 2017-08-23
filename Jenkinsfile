@Library('Credentials')
import io.tray.Credentials

def x = Credentials.GitHub()

pipeline {
  agent any

  stages {
    stage('build') {
      environment {
        DOCKER_REGISTRY = credentials('NPM_TOKEN')
      }
      
      steps {
        sh 'echo ${NPM_TOKEN}'
      }
    }
  }
}
