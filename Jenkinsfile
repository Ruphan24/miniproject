pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/Ruphan24/miniproject.git'
            }
        }

        stage('Deploy Website') {
            steps {
                sh '''
                sudo cp -r * /var/www/html/
                '''
            }
        }

    }
}
