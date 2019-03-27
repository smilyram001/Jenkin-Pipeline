pipeline {
	agent any

	stages {
	    stage('Checkout') {
	        steps {
				checkout scm			        }
		    }
		stage('Build') {
	        steps {
				sh '/home/ramesh/Jenkins-New/apache-maven-3.6.0/bin/mvn install'
	        }
		}
		stage('Deployment') {
			steps {
				sh 'scp /home/ramesh/.jenkins/workspace/GAmutkart-Ansar/target/gamutkart.war QATEAM@172.17.0.2:home/QATEAM/apache-tomcat-9.0.16/webapps'
				sh 'echo deployment is succussful!'
			}
		}

	}
}
