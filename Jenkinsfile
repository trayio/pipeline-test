pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('build') {
      steps {
        sh "echo ${BRANCH_NAME}"
      }
    }
  }
}
