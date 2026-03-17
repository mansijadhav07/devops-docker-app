pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/YOUR-USERNAME/devops-docker-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 devops-app'
            }
        }
    }
}
