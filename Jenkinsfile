pipeline {
    agent any
 
    stages {
 
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Ruphan24/miniproject.git'
            }
        }
 
        stage('Build Docker Image') {
            steps {
                sh 'docker build --no-cache -t sample-image .'
            }
        }
 
        stage('Run Docker Container') {
            steps {
                sh '''
                docker stop sample || true
                docker rm sample || true
                docker run -d -p 9090:80 --name sample sample-image
                '''
            }
        }
    }
}
