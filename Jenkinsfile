pipeline {
    agent any
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }

    stages {
        stage('Git checkout') {
            steps {
              git branch: 'main', url: 'https://github.com/Ejoumalai/Petclinic.git'
            }
        }
        
        stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
         stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
    }
}
