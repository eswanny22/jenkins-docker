pipeline {
    agent {
    // this image provides everything needed to run Cypress
    docker {
      image 'cypress/included:latest'
    }
  }

  stages {
    stage('build and test') {

      steps {
        sh 'npm cache clean --force'
        sh 'npm ci'
        sh 'npx cypress run'
      }
    }
  }
}
