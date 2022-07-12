#Jenkinsfile.json


pipeline {
    
    agent {
        label   "Jenkins-slave-linux-1"
    }
    
    stages  {
        stage('SCM')  {
            steps  {
                git 'https://github.com/vimallinuxworld13/jenkins-docker-maven-java-webapp.git'
            }
            
        }
         
        stage('Build on Mvn package')  {
            steps {
                sh 'mvn clean package'
            }
        }    

        stage('Build Docker OWN images') {
            steps {
                
                sh "sudo docker build -t vijkes/javaweb:${BUILD_TAG} ."
                //sh "${env.BUILD_NUMBER}"
                //sh 'whoami'
            }
        }
        
        stage('Push image to Docker') {
            steps {
                withCredentials([string(credentialsId: 'DOCKER_JENKINS_PWD', variable: 'NEWDOCJENTECHCOM')]) {
    // some block

            
                sh "sudo docker login -u vijkes -p ${NEWDOCJENTECHCOM}"
                 
                sh "sudo docker push vijkes/javaweb:${BUILD_TAG}"
                
                sh "sudo docker rmi vijkes/javaweb:${BUILD_TAG}"
               
            }
        }
        }         
    
    }
}
