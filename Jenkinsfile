pipeline {
    agent any 
    tools {
        maven "maven1"
    }
    stages {
        stage('clean workspace') {
            steps{
                cleanWs()
        
            }    
        }

    }
    stage ('git checkout1') {
        steps {
            git branch: 'main', url: 'https://github.com/kannanomyGIT/carrom.git'
        }
    }
    stage ('compile') {
        steps {
            sh 'mvn compile'
        }
    }
    stage ('test') {
        steps {
            sh 'mvn test'
        }
    }
    stage ('package') {
        steps {
            sh 'mvn package'
        }
    }
}