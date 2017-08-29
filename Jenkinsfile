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
          // AUTHOR = sh(returnStdout: true, script: "git log -1 | sed -ne 's/Author: \\(.*\\)<.*/\\1/p'").trim()
          // return AUTHOR == "BarryJenkins"
          return 0 != sh(script: "git log -1 | grep -q BarryJenkins", returnStatus: true)
        }
      }
          
      steps {
        sh 'echo hello'
      }
    }

    stage('two') {
      steps {
        sh 'echo two'
      }
    }
    stage('three') {
      steps {
        sh 'echo three'
      }
    }
    stage('four') {
      steps {
        sh 'echo four'
      }
    }
  }
}
