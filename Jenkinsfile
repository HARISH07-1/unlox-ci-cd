pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/HARISH07-1/unlox-ci-cd.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-cd-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'docker stop myapp || true'
                sh 'docker rm myapp || true'
            }
        }

        stage('Run New Container') {
            steps {
                sh 'docker run -d -p 8080:80 --name myapp ci-cd-app'
            }
        }
    }
}
