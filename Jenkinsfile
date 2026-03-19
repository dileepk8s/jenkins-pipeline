pipeline {
    agent any 
    stages {
        stage ('build') {
            steps {
                // sample command for eccho first pipeline job//
                echo  "hello this is build step modified by Dileep"
            }
        }
        stage ('test') {
            steps {
                //this is first test stage for pipeline job//
                echo "this is first test job for pipeline"
            }
        }
        stage ('docker') {
            steps {
                // this sfor docker stage for pipeline //
                echo "this is first docker job for pipeline"
            }
        }
    }
}
