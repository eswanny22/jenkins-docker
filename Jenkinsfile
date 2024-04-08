pipeline {
  agent any
  tools {nodejs "nodejs"}
  stages {
    stage('build and test') {

      steps {
        sh 'npm ci'
        sh 'npx cypress run'
      }
    }
  }
}
