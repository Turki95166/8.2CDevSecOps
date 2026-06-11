pipeline {
    agent any

    tools {
        nodejs 'NodeJS'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Turki95166/8.2CDevSecOps.git'
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

        stage('Generate Coverage Report') {
            steps {
                bat 'npm run coverage'
            }
        }

        stage('NPM Audit (Security Scan)') {
            steps {
                bat 'npm audit'
            }
        }
    }
}
