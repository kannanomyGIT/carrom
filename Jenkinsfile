pipeline {
    agentany 
    tools {
        maven "maven1"
    }
    stages {
        stage('clean workspace') {
            cleanWs()
        }
    }
    stage ('git checkout') {
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