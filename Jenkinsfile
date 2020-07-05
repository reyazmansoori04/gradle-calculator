pipeline {
     agent any
	
	tools{
	gradle 'GRADLE_4.5.1'
		maven 'MAVEN_3.6.3'
	}
     stages {
          stage("run frontend") {
               steps {
		       echo 'executing yarn....'
		       nodejs('Node-10.17') {
		       sh 'yarn install'
		       }
               }
          }
	      stage("run another frontend tools") {
               steps {
		       echo 'executing npm....'
		       nodejs('Node-10.17') {
		       sh 'npm install'
		       }
               }
          }
	           stage("run backend") {
               steps {
		       echo 'executing gradle....'
	
			       sh './gradlew -v'
		       
                
               }
          }
         
	
}
}
