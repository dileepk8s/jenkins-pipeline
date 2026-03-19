pipeline{
    agent any
    stages {
        stage ('firststage') {
            steps {
                echo 'hello pringing hostname where the stage excuting'
                sh 'hostname -i'
            }
        }
        stage ('secondstage'){
            agent {
                label 'apps-slave'
            }
            steps {
                echo 'hello printing hostname where this stage excuting'
                sh 'hostname -i'
            }
        }
    }
}
