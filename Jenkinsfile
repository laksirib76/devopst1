pipeline {
  agent {
    node {
      label 'dl1'
    }
  }
 stage('Build') {
        def mvn_version = 'M3'
        withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
        sh 'sh \'mvn clean install -Dlicense.skip=true\''
         }
   }
}
