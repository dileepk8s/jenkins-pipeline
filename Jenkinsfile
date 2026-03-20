pipeline {
    agent any
    tools {
        // this name should match the name configured in tools section
        maven 'maven-3.8.9'
    }
    stages {
        stage ('build') {
            steps {
                echo "this is maven verification"
                sh 'mvn --version'
            }
        }
    }
}
