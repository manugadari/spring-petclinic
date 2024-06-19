pipeline {
  agent any

    stages {
    stage('checkout') {
      steps {
        git 'https://github.com/manugadari/spring-petclinic'
      }
    }
    stage('Build') {
      steps {
        sh "python3 snyk.py " +
           "--scan-for-push"
      }
    }
  }
}
