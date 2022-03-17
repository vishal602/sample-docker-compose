pipeline {
  agent {
    node {
        label 'Jenkins-Slave-138'
    }
}
      
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
        sh 'docker-compose up -d'
        sh 'docker-compose ps'
      }
    }
  }
}
