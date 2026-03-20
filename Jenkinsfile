pipeline {
    agent any
    stages {
        stage ('build') {
            steps {
                //declarative
                echo "this is a build stage"
                sh 'hostname -i'
            }
        }
        stage ('groovrystage') {
            steps {
                script {
                    //logic 
                    // varible definition
                    // def variable = "value"
                    def course = 'docker'
                    // there are various way to call variable.
                    if (course == "k8s")
                    println("thanks for enrolling into ${course} course")
                    else 
                    println ("do join for k8s")
                
                }
            }
        }
    }
}
