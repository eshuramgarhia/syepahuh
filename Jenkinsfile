pipeline {
    agent any

    environment {
        NODE_ENV = 'any'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git 'https://github.com/eshuramgarhia/syepahuh.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Start Server') {
            steps {
                sh 'npm start'
            }
        }
    }
}
