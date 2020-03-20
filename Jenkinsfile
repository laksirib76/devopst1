pipeline {
  agent none
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
      }
    }

    stage('Testing') {
      steps {
        sh 'mvn sonar:sonar -Dsonar.host.url=http://sonarqube-1:9000 -Dlicense.skip=true'
      }
    }

  }
}