pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/aroocho/nodejs-devops-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test || true'
            }
        }

        stage('Run App') {
            steps {
                sh 'node app.js'
            }
        }
    }
}
