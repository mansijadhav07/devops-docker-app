pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t portfolio-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f portfolio || true'
                sh 'docker run -d -p 5000:80 --name portfolio portfolio-app'
            }
        }
    }
}
