pipeline {

agent any

stages {
	stage ('SCM') {
		steps	{
			  echo "git pulling code for java app1"
			  git "git pulling code for java app2"
			}
		}
	
	
	stage('Deploy') {
		steps {
			echo "deploying my code"
		      }
		}
	stage('Test') {	
		steps {
			echo "test final app for prod"
		      }
		}
}

}