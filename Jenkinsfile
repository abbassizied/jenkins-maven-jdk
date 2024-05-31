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
                withMaven(
                    // Maven installation declared in the Jenkins "Global Tool Configuration"
                    maven: 'maven-3',
                    // Maven settings.xml
                    mavenSettingsConfig: 'my-maven-settings') {
                        // Run the maven build
                        sh "mvn clean verify"
                    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe & FindBugs & SpotBugs reports...
            }
        } 
        stage('What\'s next?') {
            steps {
                echo 'What\'s next?' 
            }
        }
    }
}    
