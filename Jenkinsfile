pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/AGL2304/MonAppSimple.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('my-app')
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    docker.image('my-app').inside {
                        sh 'node app.js &'
                    }
                }
            }
        }
    }
}
