pipeline {
  agent {
    label 'app-slave'
  }

  environment {
    DEPLOY_TO = 'production'
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Dileep', description: 'Who should I say hello to?')
  }

  stages {

    stage('deploy-stage') {
      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "alice,bob"
      }
      steps {
        echo "Hello, ${params.PERSON}, nice to meet you."
      }
    }

    stage('Example') {
      when {
        allOf {
          branch 'production'
          environment name: 'DEPLOY_TO', value: 'production'
        }
      }
      steps {
        echo "deploying to prod env"
      }
    }

  }
}
