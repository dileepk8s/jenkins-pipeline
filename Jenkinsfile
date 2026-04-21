pipeline {
  agent {
    label 'app-slave'
  }
  environment {
    DEPLOY_TO = 'production'
  }
  stages {
    stage ('Deploy') {
      steps {
        echo "***Deploy to Dev environment****"
      }
    }
    stage ('PedDeploy') {
      steps {
        echo "****Deploy to prod Environment*****"
      }
    }
  }
}
