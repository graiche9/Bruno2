pipeline {
  agent any
  stages {
    
    stage('Install Bruno CLI') {
      steps {
        sh 'npm install -g @brunoc/cli'
    }

    stage('run collection'){
       steps{
        sh 'bruno run ./collections/GetUsers'
        }
    }
    
  }
}
}