pipeline {

agent any

stages {
	stage ('SCM') {
		steps	{
			  echo "git pulling code for java app2"
			  echo "git pullling code for java app23"
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