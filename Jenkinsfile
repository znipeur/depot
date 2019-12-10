pipeline{
	agent any
	tools{
	maven 'Maven 3'
	jdk 'jdk1.8.0_162'
	}
	stages {
		stage('Build'){
		steps {
		bat 'mvn compiler:compile'
		}
		
		}
		}
	
}
