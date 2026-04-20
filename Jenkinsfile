pipeline {
  agent {
    label 'app-slave'
  }
  environment {
    GIT_CREDS = credentials ('git_pat_creds') 
    //username and passwd  ====> get stored in GIT_CREDS 
  }
  stages {
    stage ('creds-test') {
      steps {
        echo "printing credentials"
        //how can we call the user name from GIT_CREDS
        echo "username is ${GIT_CREDS_USR}"
        // how can we call the password form the GIT_CREDSd
        echo "password is ${GIT_CREDS_PSW}"
      }
    }
  }
}
