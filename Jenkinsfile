     pipeline {
       agent any
              stages {
                   stage('Clone') {
                         steps {
                            git credentialsId: 'Github', url: 'https://github.com/Ijaz0059/welcometoskillrary.git'
                            }
                         }
                   stage('Build') {
                            steps {
                                sh "mvn clean install"   
                            }
                         }
		      stage('Deploy to Tomcat'){
			      steps{
                               sh "copy /var/lib/jenkins/workspace/NewJob/webapp/target/webapp.war "/home/ec2-user/apache-tomcat-9.0.58/webapps""
"
				    
				   }
		      }
                      
		      
	          }
     }
