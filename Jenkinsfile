pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo "Verificando branch y repo"
                git branch: 'develop', url: 'https://github.com/FacuMiglio/bootcamp-devops-git.git'
            }
        }

        stage('Deploy Test') {
            steps{
                echo "Desplegando en Apache..."
                // Copiar archivos a WebServer1 - Test
                echo "Copiando en WebServer - TEST"
                sh 'scp -o StrictHostkeyChecking=no -r * facu@192.168.100.20:/var/www/html/'
                }
        }

        stage('Checkout Prod') {
            steps {
                echo "Verificando branch y repo"
                git branch: 'main', url: 'https://github.com/FacuMiglio/bootcamp-devops-git.git'
            }
        }
        stage('Deploy Test') {        
            steps{
                // Copiar archivos a WebServer1 - Prod
                echo "Copiando en WebServer - PROD"
                sh 'scp -o StrictHostkeyChecking=no -r * facu@192.168.100.21:/var/www/html/'
            }

        }
    }
}
