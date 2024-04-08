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
        sh 'npx cypress run'
      }
    }
  }
}
