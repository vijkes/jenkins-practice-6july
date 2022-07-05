pipeline {

agent any

stages {
	stage ('SCM') {
		steps	{
			  echo "git pulling code for java app2"
			  git 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
			}
		}
	
	
	stage('Build') {
		steps {
			sh 'mvn clean package'
		      }
		}
	stage('Test') {	
		steps {
			echo "test final app for prod"
		      }
		}

	stage('Deploy to Prod') {	
		steps {
			echo "final app for production"
		      }
		}
}

}