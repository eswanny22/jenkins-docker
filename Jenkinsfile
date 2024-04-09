pipeline {
          environment {
        // we will be recording test results on Cypress Cloud
        // to record we need to set an environment variable
        // we can load the record key variable from credentials store
        // see https://jenkins.io/doc/book/using/using-credentials/
        tools {
          'org.jenkinsci.plugins.docker.commons.tools.DockerTool' 'docker'
        }
      }
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
        sh 'npx cypress run'
      }
    }
  }
}
