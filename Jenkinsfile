pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t skyforge-cloud .'
            }
        }

        stage('Stop Old Container') {
            steps {
                bat 'docker stop skyforge-container || exit 0'
                bat 'docker rm skyforge-container || exit 0'
            }
        }

        stage('Run New Container') {
            steps {
                bat 'docker run -d -p 8081:80 --name skyforge-container skyforge-cloud'
            }
        }

    }
}