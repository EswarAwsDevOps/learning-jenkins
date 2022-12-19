pipeline {
  agent any

  environment {
    ABC="abc"
  }

  stages {
    stage('New') {
      environment {
        XYZ="xyz"
      }
      steps {
        echo 'Hello World'
        echo "${XYZ}"
      }
    }
  }

  post {
    always {
      echo 'OK'
    }
  }
}

