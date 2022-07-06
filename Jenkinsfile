pipeline {

agent any

stages {
	stage ('SCM') {
		steps	{
			  echo "git pulling code for java app_new"
			  git 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
			}
		}
	

	stage ('Deploy') {
		steps	{
			  echo "deploying my code"
			 
			}
		}
	stage ('Test') {
		steps	{
			  echo "test my final webapp"
			
			}
		}
	stage('Deploy to Prod') {	
		steps {
			echo "final app for production"
		      }
		}
	}
}