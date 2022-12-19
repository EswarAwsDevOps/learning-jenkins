pipeline {
  agent any

  options { buildDiscarder(logRotator(numToKeepStr: '1')) }

  environment {
    ABC="abc"
    SSH = credentials("SSH")
  }

  stages {
    stage('New') {
      environment {
        XYZ="xyz"
      }
      steps {
        echo 'Hello World'
        echo "${XYZ}"
        echo "${SSH}"
      }
    }
  }

  post {
    always {
      echo 'OK'
    }
  }
}

