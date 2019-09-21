pipeline {
    agent any 
    stages {
        stage('-----Clean-----') { 
            steps {
               def mvnHome= tool name: 'm6', type: 'maven'
                sh "${mvnHome}/bin/mvn clean"
            }
        }
        stage('-----Test-----') { 
            steps {
                sh "mvn test"
            }
        }
        stage('----Deploy-----') { 
            steps {
                sh "mvn package"
            }
        }
    }
}
