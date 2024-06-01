 pipeline {
    agent any 
    tools {
        maven 'maven397'
    }
	 
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abbassizied/jenkins-maven-jdk.git'
            }
        }
        stage('Testing OpenJDK Installation') {
            steps {
               sh "which java"
               sh "java -version"
            }
        }       
        stage('Testing Maven Installation') {
            steps {
                withMaven {
		    sh "mvn --version"
                } 
            }
        } 
        stage('What\'s next?') {
            steps {
                echo 'What\'s next?' 
            }
        }
    }
}    
