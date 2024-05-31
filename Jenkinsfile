 pipeline {
    agent any 
    
    tools {
        jdk 'jdk17'
        maven 'maven3'
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/abbassizied/jenkins-maven-jdk.git'
            }
        }
        stage('Compile') {
            steps {
               sh "mvn clean compile"
            }
        }
        stage('What\'s next?') {
            steps {
                echo 'What\'s next?' 
            }
        }
    }
}    
