@Library('Credentials')
import io.tray.Credentials

def x = Credentials.GitHub()

pipeline {
  agent any

  stages {
    stage('build') {
      environment {
        NPM_TOKEN = credentials('8c59cc7c-077b-4115-a136-e5b64142345a')
        SECRET_TEXT = credentials('SECRET_TEST')
      }
      
      steps {
        sh 'echo ${NPM_TOKEN}'
      }
    }
  }
}
