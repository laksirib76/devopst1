pipeline {
  agent {
    node {
      label 'dl1'
    }

  }
  stages {
    stage('Build') {
        def mvn_version = 'maven3'
        withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
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
