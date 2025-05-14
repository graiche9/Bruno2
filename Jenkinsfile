pipeline {
    agent {
        docker {
            image 'node:18-alpine'
            args '-u root'
        }
    }
    stages {
        stage('Install Bruno CLI') {
            steps {
                sh 'npm install -g bru'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Run Bruno Test') {
            steps {
                sh 'bru run GetUsers.bru --reporter-html results.html'
            }
        }
    }
}
