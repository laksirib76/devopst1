pipeline {
  agent {
    node {
      label 'dl1'
    }
  }
  stages {
 stage('Build') {
        def mvn_version = 'M3'
        withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
        sh 'sh \'mvn clean install -Dlicense.skip=true\''
         }
 }
   }
}
