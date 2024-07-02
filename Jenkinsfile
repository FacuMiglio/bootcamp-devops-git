pipeline {
    agent any
    stages {
        stage('Preparation') {
            steps {
                // Limpia el workspace antes de iniciar el build
                cleanWs()
                echo "Preparación del entorno"
            }
        }
        stage('Build') {
            steps {
                echo "Verificando branch y repo"
                sh 'git clone https://github.com/FacuMiglio/bootcamp-devops-git.git'
                sh 'scp -o StrictHostkeyChecking=no -r * facu@192.168.100.20:/var/www/html/'
            }
        }

        }
    }