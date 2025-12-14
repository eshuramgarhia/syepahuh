  pipeline {
    agent any

    tools {
        nodejs 'Nodejs'   // Jenkins > Global Tool Configuration ch NodeJS name
    }

    environment {
        NODE_ENV = 'any'
    }

    stages {

        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/eshuramgarhia/syepahuh.git'
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

        stage('Build (optional)') {
            steps {
                echo 'No build step for backend'
            }
        }

        stage('Start App') {
            steps {
                sh 'npm start'
            }
        }
    }

    post {
        success {
            echo '✅ Build Successful'
        }
        failure {
            echo '❌ Build Failed'
        }
    }
}
