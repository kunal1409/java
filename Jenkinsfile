pipeline {
  agent {label 'slave'}
 
  stages {
    stage ('Build') {
      steps {
      sh 'mvn clean install -f java/pom.xml'
      }
    }
   
    stage ('DEV Deploy') {
      steps {
      echo "deploying to DEV Env "
      deploy adapters: [tomcat9(credentialsId: '268c42f6-f2f5-488f-b2aa-f2374d229b2e', path: '', url: 'http://your_public_dns:8080')], contextPath: null, war: '**/*.war'
      }
    }
    
