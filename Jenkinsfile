@Library('Credentials')
import io.tray.Credentials

def x = Credentials.GitHub()

pipeline {
  agent any

  stages {
    stage('build') {
      environment {
        DOCKER_REGISTRY = credentials('Docker Hub')
      }
      
      steps {
        sh "echo ${DOCKER_REGISTRY}"
        sh "echo ${DOCKER_REGISTRY_USR}"
        sh "echo ${DOCKER_REGISTRY_PSW}"
      }
    }
  }
}
