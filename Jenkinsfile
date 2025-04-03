pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/vickydgh/jenkins.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t simple-web-app .'
            }
        }
        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8081:80 --name webapp simple-web-app'
            }
        }
    }
}
