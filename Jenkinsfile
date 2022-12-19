pipeline {
  agent any

  options {
    buildDiscarder(logRotator(numToKeepStr: '1'))
    ansiColor('xterm')
  }

  triggers {
    //cron('0 * * * *')
    pollSCM('* * * * *')
  }

  parameters {
    string(name: 'APP_URL', defaultValue: '', description: 'App URL')
  }

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
        echo "${APP_URL}"
      }
    }
  }

  post {
    always {
      echo 'OK'
    }
  }
}

