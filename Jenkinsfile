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
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

    }
  }
