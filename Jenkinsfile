pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/rbeg/appone.git', branch: 'master', credentialsId: 'jenkins_ci')
      }
    }
    stage('Build') {
      steps {
        bat 'npm install'
      }
    }
    stage('Unit Test') {
      steps {
        bat 'npm run test'
      }
    }
  }
}