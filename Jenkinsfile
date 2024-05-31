 pipeline {
    agent any 
  
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abbassizied/jenkins-maven-jdk.git'
            }
        }
        stage('Testing OpenJDK Installation') {
            steps {
               sh "which java"
            }
        }       
        stage('Testing Maven Installation') {
            steps {
               sh "mvn -v"
            }
        } 
        stage('What\'s next?') {
            steps {
                echo 'What\'s next?' 
            }
        }
    }
}    
