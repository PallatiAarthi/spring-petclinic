pipeline {
  agent {
    node {
      label 'Test'
    }

  }
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

  }
}