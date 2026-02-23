pipeline {
    agent any
    stages{
        stage('Clone Code'){
            steps{
                git branch: 'main', url: 'https://github.com/Rohithkumar-2006/DevOps-Project-Two-Tier-Flask-App'
            }
        }
        stage('Build Docker Image'){
            steps{
                sh 'docker build -t myflaskapp:latest .'
            }
        }
        stage('Deploy with Docker Compose'){
            steps {
                sh 'sudo chmod -R 755 static'
                sh 'docker compose down || true'
                sh 'docker compose up -d --build --force-recreate'
            }
        }

    }
}