pipeline {
  agent { label 'office' }

  stages {
    stage('build') {
      agent {
        docker {
          label 'office'
          image 'tray/sbt:v3'
        }
      }

      steps {
        checkout scm
      }
    }
  }
}