pipeline {
  agent any
  tools {
    mavnen 'maven-3.8.9'
  }
  stages {
    stage ('build stage') {
      steps {
        echo "testing the maven version in globel"
        sh 'mvn --version'
      }
    }
    stage ('maven custom-stage'){
      tools {
        jdk 'open-jdk'
      }
      steps {
        echo "this is custom java version"
        sh 'mvn --version'
      }
    }
  }
}
