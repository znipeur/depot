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
                stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
		stage('couverture') {
            steps {
               
                bat 'mvn cobertura:cobertura '
                
            }
             
        }
                stage('Document') {
            steps {
               
                bat 'mvn site '
                
            }
             
        }
                stage('Packaging') {
            steps {
               
                bat 'mvn package '
                
            }
             
        }
                 stage('Installing') {
            steps {
               
                bat 'mvn install '
                
            }
             
        }
	}
}
