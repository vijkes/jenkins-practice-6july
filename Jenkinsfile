pipeline {

agent any

stages {
	stage ('SCM') {
		steps	{
			  echo "git pulling code for java app_new"
			  git 'https://github.com/vimallinuxworld13/simple-java-maven-app.git'
			}
		}
	

	stage ('Build') {
		steps	{
			  sh 'sudo yum install maven -y'
			  sh 'mvn clean package'
			 
			}
		}
	stage ('Deploy') {
		steps	{
			  sh 'java -jar target/*.jar'  
			
			}
		}
	stage('Deploy to Prod') {	
		steps {
			echo "final app for production"
		      }
		}
	}
}