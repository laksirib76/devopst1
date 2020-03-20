pipeline {
  agent {
    node {
      label 'dl1'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install -Dlicense.skip=true'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn sonar:sonar -Dsonar.host.url=http://sonarqube-1:9000 -Dlicense.skip=true'
      }
    }

  }
  tools {
    maven 'maven3'
  }
}