pipeline {
    agent {
        label 'app-slave'
    }
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('deploy-stage') {
            stage('Example') {
                input {
                    message "Should we continue?"
                    ok "Yes, we should."
                    submitter "alice,bob"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                    }
                }
                steps {
                    echo "Hello, ${PERSON}, nice to meet you."
                }
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
}
