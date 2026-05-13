pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Ruphan24/miniproject.git'
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                sudo cp -r index.html style.css script.js /var/www/html/
                '''
            }
        }

    }
}
