pipeline {
  agent any

  options {
    ansiColor('xterm')
    timestamps()
  }

  stages {
    stage('test') {
      steps {
        script {
          def x = "hello"
          sh "echo ${x}"
        }
      }
    }
  }
}
