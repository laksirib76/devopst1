pipeline {
   agent {
    node {label 'dl1'}
        }
    tools {
        maven 'maven3'
    }
  stages {
      stage('Build') {
         steps {
        sh 'mvn clean install -Dlicense.skip=true'
      }
    }

  }
}
