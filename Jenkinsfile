pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                    sh 'javac OlaUnicamp.java'
            }
        }

        stage('Run') {
            steps {

                    sh "docker run java OlaUnicamp"
            }
        }
    }

    post {
        success {
            echo 'Pipeline executado com sucesso!'
        }
        failure {
            echo 'O pipeline falhou.'
        }
    }
}

