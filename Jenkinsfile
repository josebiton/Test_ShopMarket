pipeline {
    agent any

    stages {
        stage('Preparacion') {
            steps {
                git branch: 'main', url: 'https://github.com/josebiton/Test_ShopMarket.git'
                echo 'Pulled from GitHub successfully'
            }
        }


        stage('Verifica version php') {
            steps {
                sh 'php --version'
            }
        }

          
        stage('Deploy php') {
            steps {
                sh 'docker compose up -d'
            }
        }
    }
}
