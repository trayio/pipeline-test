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
          AUTHOR = sh script: "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'", returnStdout: true
          return AUTHOR == "Luka Furlan"
        }
      }
          
      steps {
        sh script: "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'", returnStdout: true
      }
    }

    stage('test') {
      steps {
        sh script: "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'"
      }
    }
  }
}
