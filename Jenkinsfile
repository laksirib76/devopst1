pipeline {
  agent {
    node {
      label 'dl1'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'sh \'mvn clean install -Dlicense.skip=true\''
      }
    }

  }
}