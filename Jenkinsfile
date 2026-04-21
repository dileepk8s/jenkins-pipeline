pipeline {
  agent {
    label 'app-slave'
  }
  environment {
    DEPLOY_TO = 'production'
  }
  stages {
    stage ('dev-stage') {
      steps {
        echo "deoplying to dev environment"
      }
    }
    stage ('pro-stage') {
      when {
        allOf {
          branch 'production'
          environment name: 'DEPLOY_TO' , value: 'production'
        }
      }
      steps {
        echo "deploytin to pro evnironment"
      }
    }

  }
}
