pipeline {
  agent any

    stages {
     stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/main']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/manugadari/spring-petclinic'
                    ]]
                ])
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
