pipeline {
    agent any

    parameters {
        string(name: 'ENV_NAME', defaultValue: 'dev', description: 'Environment to deploy')
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run test stage?')
        choice(name: 'ACTION', choices: ['build', 'deploy','Approve'], description: 'Select action')
    }

    stages {
        stage('Build') {
            when {
                expression { params.ACTION == 'build' || params.ACTION == 'deploy' }
            }
            steps {
                echo "Building application for ${params.ENV_NAME}"
            }
        }

        stage('Test') {
            when {
                expression { params.RUN_TESTS == true }
            }
            steps {
                echo "Running tests..."

                script {
                    if (params.ENV_NAME == 'prod') {
                        echo "Running extra production checks"
                    } else {
                        echo "Running normal test checks"
                    }
                }
            }
        }

        stage('Approval') {
            when {
                expression { params.ACTION == 'deploy' && params.ENV_NAME == 'prod' }
            }
            steps {
                input message: 'Deploy to production?', ok: 'Approve'
            }
        }

        stage('Deploy') {
            when {
                expression { params.ACTION == 'deploy' }
            }
            steps {
                script {
                    if (params.ENV_NAME == 'dev') {
                        echo "Deploying to DEV"
                    } else if (params.ENV_NAME == 'qa') {
                        echo "Deploying to QA"
                    } else {
                        echo "Deploying to PROD"
                    }
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline finished"
        }
        success {
            echo "Pipeline succeeded"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}

