pipeline {
         agent any
         stages{        
           stage('-----Clone Repo-----') { 
             steps{ 
                git "https://github.com/mayanks44/FirstMVNProject"
            }
         }
        stage('-----Clean-----') { 
             steps{
               def mvnHome = tool name: 'm6', type: 'maven'
                sh "${mvnHome}/bin/mvn clean"
             }
         }
        stage('-----Test-----') { 
              steps{
                def mvnHome = tool name: 'm6', type: 'maven'
                sh "${mvnHome}/bin/mvn test"
              }
         }
        stage('----Deploy-----') { 
              steps{
                def mvnHome = tool name: 'm6', type: 'maven'
                sh "${mvnHome}/bin/mvn package"
              }
         }
    }
}
