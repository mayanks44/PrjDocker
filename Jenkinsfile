node {
         stage('-----Clone Repo-----') { 
                git "https://github.com/mayanks44/FirstMVNProject"
            }
        stage('-----Clean-----') { 
               def mvnHome = tool name: 'm6', type: 'maven'
                sh "${mvnHome}/bin/mvn clean"
        }
        stage('-----Test-----') { 
                sh "mvn test"
        }
        stage('----Deploy-----') { 
                sh "mvn package"
        }
}
