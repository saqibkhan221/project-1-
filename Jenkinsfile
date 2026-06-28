pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Repository cloned successfully!'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t project-1-image .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker rm -f project-1-container || true'
                sh 'docker run -d --name project-1-container -p 8001:80 project-1-image'
            }
        }
    }
}
