pipeline {
    agent {label "linux"}
    stages {
        stage('Build') {
            steps {
                    sh """
                docker build OlaUnicamp.java .
                """
            }
        }

        stage('Run') {
            steps {
                    sh """
                docker run --rm OlaUnicamp.java
                """
            }
        }
    }
}
