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
          
     stage('Docker Build') {
            steps {
                sh 'docker build -t testmarket .'
            }
        }
          
        stage('Deploy php') {
            steps {
                sh 'docker-compose down'
                sh 'docker compose up -d'
            }
        }
    }
}
