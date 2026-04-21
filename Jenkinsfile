pipeline {
  agent {
    label 'app-slave'
  }
  environment {
    DEPLOY_TO = 'production'
  }
  stages {
    stage ('deploy-stage') {
      when {
        branch 'production'
        environment name: 'DEPLOY_TO', value: 'production'
      }
      steps {
        echo "deploying to prod env"
      }
    }
  }
}
