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
        sh 'npm ci'
        sh 'chown -R 503:20 "/.npm"'
        sh 'npx cypress run'
      }
    }
  }
}
