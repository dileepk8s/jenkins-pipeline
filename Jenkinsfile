pipeling {
  agent {
    label 'app-slave'
  }
  environment {
    ///keys = values
    name = 'dileep'
    course = 'docker and k8s'
  }
  stages {
    stage ('first-stage') {
      environment {
        cloud = 'aws'
      }
      steps {
        echo "welcome to ${name} "
        echo " you enrolled for ${course} course"
        echo "${name} certified in cka course"
        echo "your certified in ${cloud}"
      }
    }
    stage ('second-stabe') {
      steps {
        echo "weilcome to ${name}"
        echo "your enrolled for ${course} course"
        echo "${name} certified in k8s"
        echo "your certified in ${cloud} cloud"
      }
    }
  }
}
