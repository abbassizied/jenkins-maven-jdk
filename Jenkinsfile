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
            def mvnHome = tool name: 'Apache Maven 3.6.0', type: 'maven'
            steps {
               sh "${mvnHome}/bin/mvn -B -DskipTests clean package"
            }
        } 
        stage('What\'s next?') {
            steps {
                echo 'What\'s next?' 
            }
        }
    }
}    
