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
          def x = env.BRANCH_NAME.replace("m", "k")
          sh "echo ${x}"
        }
      }
    }
  }
}
