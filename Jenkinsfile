//this pipeling of testing salve
// globel setting applicable for all in the pipeline 
pipeline {
  agent any
  stages {
    stage ('firststage') {
      steps {
        echo "this stage should excute for master node are global lever"
        sh 'hostname'
      }
    }
    stage ('secondstage') {
      //stage settings
      agent {
        label 'app-slave'
      }
      steps {
        echo "This stage should be excute only slave node only"
        sh 'hostname -i'
      }
    }

  }
}
