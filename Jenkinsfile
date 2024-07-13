pipeline {
    agent {label "linux"}
    stages {
        stage('Build') {
            steps {
                    sh """
                docker build -t olaunicamp.java .
                """
            }
        }

        stage('Run') {
            steps {
                    sh """
                docker run --rm olaunicamp.java
                """
            }
        }
    }
}
