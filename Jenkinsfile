pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t unlox-project .'
            }
        }

        stage('Stop Old Container') {
            steps {
                bat 'docker stop unlox-cid || exit 0'
                bat 'docker rm unlox-cid || exit 0'
            }
        }

        stage('Run New Container') {
            steps {
                bat 'docker run -d -p 8086:80 --name unlox-cid unlox-project'
            }
        }
    }
}

