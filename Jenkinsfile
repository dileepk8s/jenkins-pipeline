////thi pipeline for sprcific agent 
pipeline {
  agent {
    label 'app-slave'
  }
  stages {
    stage ('buils') {
      steps {
        echo "this pipeline set up for slave machine"
      }
    }
    stage ('hostname') {
      steps {
        sh 'hostname -i'
      }
    }
  }
}
