pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''./mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://3.25.149.27:9000 \\
  -Dsonar.token=sqp_63fe1acf3131061701ce3e6d2081fb208067b49b'''
      }
    }

  }
}