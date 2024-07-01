pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Verificando branch y repo"
                sh 'git clone https://github.com/FacuMiglio/bootcamp-devops-git.git'
                sh 'scp -o StrictHostkeyChecking=no -r * facu@192.168.100.20:/var/www/html/'
            }
        }

        }
    }