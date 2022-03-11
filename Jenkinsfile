pipeline {
  agent any
  stages {
    stage("verify tooling") {
      steps {
        sh '''
          docker version
          docker info
          docker-compose version 
          curl --version
        '''
      }
    }
  
    stage('Start container') {
      steps {
        sh '''
        sh 'docker-compose up -d'
        sh 'docker-compose ps'
      }
    }
  }
}
