pipeline {
  agent any

  tools {
    maven 'maven'
  }

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
      when {
        expression {
          APP_URL == "google.com"
        }

      }
      environment {
        XYZ="xyz"
      }
      steps {
        echo 'Hello World'
        echo "${XYZ}"
        echo "${SSH}"
        echo "${APP_URL}"
        //sh 'mvn compile'
      }
    }

    stage('Example') {

      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "admin"

      }
      steps {
        echo "Hello, nice to meet you."
      }
    }

  }

  post {
    always {
      echo 'OK'
    }
  }
}


