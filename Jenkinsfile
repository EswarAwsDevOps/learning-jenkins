pipeline {
  agent any

  stages {
    stage('New') {
      steps {
        echo 'Hello World'
      }
    }
  }

  post {
    always {
      echo 'OK'
    }
  }
}

