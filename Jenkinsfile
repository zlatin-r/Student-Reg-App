pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run audit test') {
            steps {
                bat 'npm audit'
            }
        }
        stage('Run integration test') {
            steps {
                bat 'npm run test'
            }
        }
        stage('Approval for Production Deployment') {
            steps {
                script {
                    input message: 'Proceed with production deployment?', ok: 'Deploy'
                }
            }
        }
        stage('Deploy to STAGING') {
            steps {
                echo 'Deployn to Staging'
            }
        }
        stage('Deploy to PRODUCTION') {
            steps {
                echo 'Deployn to Production'
            }
        }
    }
}
