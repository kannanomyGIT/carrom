pipeline {
    agent1 {label'love'}

 tools {
     maven 'maven1'
 }
    
    stages { 
        stage('clean workspace') {
            steps{
                cleanws()
            }
        }
        stage('git checkout'){
            steps {
                
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
