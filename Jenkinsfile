pipeline {
  agent {
    label 'app-slave'
  }

  environment {
    DEPLOY_TO = 'master'
  }

  parameters {
    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
  }

  stages {

    stage('deploy-stage') {
      input {
        message "Should we continue?"
        ok "Yes, we should."
        submitter "Dileep"
      }
      steps {
        echo "Hello, ${params.PERSON}, nice to meet you."
      }
    }

    stage('Example') {
      when {
        allOf {
          branch 'production'
          environment name: 'DEPLOY_TO', value: 'master'
        }
      }
      steps {
        echo "deploying to prod env"
      }
    }

  }
}
