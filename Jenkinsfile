pipeline {
  agent any
  stages {
    stage ('build') {
      steps {
        retry (3) {
          echo "this is retry example"
          erro "this is error for retry example"
        }
        echo "this is retry pipeline"
      }
    }
  }
}
