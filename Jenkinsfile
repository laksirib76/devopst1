pipeline {
  agent {
    node {
      label 'dl1'
    }

  }
  stages {
    stage('Build') {
      def mvn_version = 'maven3'
      steps {
        sh 'sh \'mvn clean install -Dlicense.skip=true\''
      }
    }

  }
}
