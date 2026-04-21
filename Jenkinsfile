pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                script {
                    def skipBuild=env.SKIP_BUILD
                    if (skipBuild == null || skipBuild.isEmpty()) {
                        echo 'starting build ...'
                    } else {
                        echo 'skipping build ...'
                    }
                }
            }
        }
    }
}
