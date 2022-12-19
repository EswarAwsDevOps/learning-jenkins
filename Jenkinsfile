pipeline {
  agent any

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

