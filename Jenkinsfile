pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('barry') {
      when {
        expression {
          AUTHOR = sh(returnStdout: true, script: "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'").trim()
          return AUTHOR == "Luka Furlan"
        }
      }
          
      steps {
        sh 'hello'
      }
    }
  }
}
