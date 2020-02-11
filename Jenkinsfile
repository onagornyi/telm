pipeline {
  agent none

  stages {

    stage('Build') {
      agent { docker 'node:13.8.0-alpine3.10' }
      steps {
        sh 'yarn install --ignore-engines'
      }
    }

    stage('Tests') {
      agent { docker 'node:13.8.0-alpine3.10' }
      steps {
        sh 'yarn test'
      }
    }

  }
}
