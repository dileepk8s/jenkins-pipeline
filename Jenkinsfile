pipeline {
  agent any
  tools {
    maven 'maven-3.8.9'
  }
  stages {
    stage ('maven') {
      steps {
        echo "this stage for maven version"
        sh 'mvn --version'
      }
    }
  }
}
