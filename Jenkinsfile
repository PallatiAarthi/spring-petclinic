pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://52.62.156.135:9000 \\
  -Dsonar.token=sqp_6a33a4ae6769ee52b2e029cbc33eb52ba145166e'''
      }
    }

  }
  environment {
    StaticAnalysis = ''
  }
}