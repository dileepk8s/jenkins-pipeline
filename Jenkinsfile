pipeline {
    agent {
        label = 'app-slave'
    }
    environment {
        name = 'dileep'
        course = 'k8s'
    }
    stages {
        stage ('firt-stage') {
            environment {
                cloud = 'aws'
            }
            steps {
                echo "welcome to ${name}"
                echo "your enrolled for ${course} course"
                echo "${name} certified in k8s"
                echo "your certified in ${cloud}"
            }
        }
        stage ('second-stage') {
            environment {
                name = 'john'
                cloud = 'gcp'
            }
            steps {
                echo "welcome to ${name}"
                echo "your enrolled for ${course} course"
                echo "${name} certified in cka"
                echo "your certified in ${cloud}"
            }
        }
    }
}
