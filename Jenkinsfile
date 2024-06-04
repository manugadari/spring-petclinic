pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        echo 'Building...'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing...'
        
          snykSecurity organisation: 'manugadari', projectName: 'petclinic', severity: 'high', snykInstallation: 'SNYK', snykTokenId: 'SNYK_API_TOKEN'
        
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
}
