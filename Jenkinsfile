pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run integration test') {
            steps {
                bat 'npm run test'
            }
        }
    }
}
