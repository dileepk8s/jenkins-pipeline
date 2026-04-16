pipeline {
  agent any
  stages {
    stage ('Frist stage') {
      steps {
        echo "printing the hostname where this stage will execute"
        sh 'hostname  -i'
      }
    }
    stage ('second stage') {
      steps {
        echo "printing the hostname where this stage will exuecute"
        sh 'hostname -i'
      }
    }
  }
}
