pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compilação do arquivo Java
                    sh 'javac OlaUnicamp.java'
                }
            }
        }

        stage('Run') {
            environment {
                // Define a variável para o nome do container Docker
                CONTAINER_NAME = 'OlaUnicamp'
            }
            steps {
                script {
                    // Executa o arquivo Java no container Docker
                    sh "docker exec java OlaUnicamp"
                }
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

