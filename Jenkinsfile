pipeline {
    agent any 
    stages {
        stage('Test Docker Permissions') {
            steps {
                sh 'id'
                sh 'groups'
                sh 'ls -la /var/run/docker.sock'
                sh 'docker ps'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app .'
            }
        }
    }
}

