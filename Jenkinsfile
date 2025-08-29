pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'No build needed for static HTML project'
      }
    }
    stage('Deploy') {
      steps {
        sh '''
          rm -rf /var/www/html/*
          cp -r * /var/www/html/
        '''
      }
    }
  }
}
