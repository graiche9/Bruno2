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
       
        stage('Run Bruno Test') {
            steps {
                sh 'bru run tests/ --reporter-html results.html'
            }
        }
    }
}
