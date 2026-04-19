pipeline {
  agent {
    label 'app-slave'
  }
  environment {
    //key= value
    name = "dileep"
    course = "docker and k8s"
  } 
  stages {
    stage ('build') {
      steps {
      echo "welcome to ${name}"
      echo "you enrolled for ${course} course"
      echo "${name} is certified in cka"
      }
    }
  }
}
