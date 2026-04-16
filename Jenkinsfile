// basic env pipeline
pipeline {
  agent any
  stages {
    stage ('build') {
      steps {
        echo "this is for globel level course"
        sh 'hostname -i'
      }
    }
    stage ('secondstage') {
      steps {
        script {
          def course = "k8s"
          if (course == "Docker")
          println ("thanks for enrolling  for ${course}")
          else 
          println ("Do join for ${course}")
        }
      }
    }
  }
}
