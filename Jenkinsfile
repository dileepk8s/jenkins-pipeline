//using when conditions in pipeline
pipeline {
  agent {
  label 'app-slave'
  }
  environment {
    DEPLOY_TO = 'production'
  }
  stages {
    stage ('stage-1') {
      when {
        environment name: 'DEPLOY_TO' , value: 'dev'
      }
      steps {
        echo "printing some data"
      }
    }
  }
}
