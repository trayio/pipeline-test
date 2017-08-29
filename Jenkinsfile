def pull

pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('build') {
      steps {
        script {
          pull = checkout scm

          sh 'echo ${pull}'
        }
      }
    }
  }
}
