pipeline {
  agent {
    node {
      label 'dl1'
    }

  }
  stages {
    def mvn_version = 'maven3'
    stage('Build') {
         steps {
        sh 'sh \'mvn clean install -Dlicense.skip=true\''
      }
    }

  }
}
