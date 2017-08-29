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
          AUTHOR = sh "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'"
          return AUTHOR == "Luka Furlan"
        }
      }
          
      steps {
        sh "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'"
      }
    }

    stage('test') {
      steps {
        sh "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'"
      }
    }
  }
}
