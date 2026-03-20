pipeline {
    agent any
    tools {
        maven 'maven-3.8.9'
    }
    stages {
        stage ('mavendefault') {
            steps {
                echo "welcome to maven section, this is default java section"
            }
        }
        stage ('custommaven') {
            tools{
                jdk 'jdk-17'
            }
            steps{
                echo "welcome to maven this is custom java section"
                sh 'mvn --version'
            }
        }
    }
}
