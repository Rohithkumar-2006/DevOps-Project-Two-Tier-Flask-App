pipeline {
    agent any
    stages{
        stage('Clone Code'){
            steps{
                git branch: 'main', url: 'https://github.com/Rohithkumar-2006/DevOps-Project-Two-Tier-Flask-App'
            }
        }
        stage('Build and Deploy with Docker Compose'){
            steps {
                sh 'docker-compose --version'
               
                sh 'docker-compose down --remove-orphans || true'
                
                sh 'docker-compose up -d --build --force-recreate'
            }
        }

    }
}