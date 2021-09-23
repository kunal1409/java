pipeline {
  agent {label 'slave'}
 
  stages {
    stage ('Build') {
      steps {
      sh 'mvn clean install -f java/pom.xml'
      }
    }
   
  }
}
