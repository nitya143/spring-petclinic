pipeline {
  agent any
  stages {
    stage('shell') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=petclinic \\
  -Dsonar.projectName=\'petclinic\' \\
  -Dsonar.host.url=http://15.206.2.43:9000 \\
  -Dsonar.token=sqp_15d11ee2d7cf882e795fb8a4a9dedf43137ede8c'''
      }
    }

  }
}