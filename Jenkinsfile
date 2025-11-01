pipeline {
    agent any
 tools {
     maven 'maven1'
 }
    stages { 
        stage('clean workspace') {
            steps{
                cleanWs()
            }
        }
        stage('git checkout'){
            steps {
                git branch: 'main', url: 'https://github.com/kannanomyGIT/carrom.git'
            }
        }
        stage('Compile') {
            steps {
            sh  'mvn compile'
            }
        }
        
        stage('Testing') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Building The Project') {
            steps {
                sh 'mvn package'
            }
        }
    }
}
