pipeline{
    agent any
    stages {
        stage('Verify integration'){
            steps{
                sh 'bru --version'
            }
        }
        stage('run all files in the collection'){
            steps{
                dir(''){
                    sh 'bru run'
                }
            }
        }
    }
}