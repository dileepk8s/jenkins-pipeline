pipeline {
    agent {
        label 'apps-slave'
    }
    stages {
        stage ('build') {
            steps {
                echo "hello-world"
            }
        }
        stage ('test') {
            steps {
                sh 'hostname -i'
            }
        }
    }
}
