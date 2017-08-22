pipeline {
  agent { label 'office' }

  stages {
    stage('build') {
      agent {
        docker {
          image 'tray/sbt:v3'
        }
      }

      steps {
        checkout scm

        sh 'sbt --version'
      }
    }
  }
}
