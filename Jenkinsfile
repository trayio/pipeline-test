@Library('Credentials')
import io.tray.Credentials

def x = Credentials.GitHub()

pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh "${x}"
      }
    }
  }
}
