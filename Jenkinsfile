pipeline {
  agent {
 label 'docker' 
    }
  stages {
    stage('build with docker') {
      agent {
        docker {
          label 'docker'
          image 'maven:3.3.3'
        }
      }
      steps {
        sh 'mvn --version'
        sh 'mvn install'
      }
    }
  }
}
