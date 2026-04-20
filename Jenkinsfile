pipeline {
  agent {
  label 'app-slave'
  }
  environment {
    DEPLOY_TO = 'production123'
  }
  stages {
    stage ('stage-1') {
      when {
        environment name: 'DEPLOY_TO' , value: 'production'
      }
      steps {
        echo "printing some data"
      }
    }
  }
}
