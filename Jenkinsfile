pipeline {
    agent any
    stages {
        stage ('build') {
            steps {
                retry (3) {
                    echo "this is retry example"
                    //replicate a failure
                    error "this is a error form retry example"
                }
            }
        }
    }
}
