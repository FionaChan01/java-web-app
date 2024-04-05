pipeline {
  agent any
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'test') { 
          sh './mvnw install org.sonarsource.scanner.maven:sonar-maven-plugin:3.9.0.2155:sonar -Dsonar.projectKey="javawebapp" -Dsonar.login="admin" -Dsonar.password="admin"'
        }
      }
    }
  }
}