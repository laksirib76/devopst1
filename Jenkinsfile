pipeline {
  agent {
    node {
      label 'dl1'
    }

  }
  stages {
    stage('Build') {
      steps {
        def mvn_version = 'maven3'
        sh 'sh \'mvn clean install -Dlicense.skip=true\''
      }
    }

  }
}
