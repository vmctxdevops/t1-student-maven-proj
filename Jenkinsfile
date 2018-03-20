pipeline {
  agent any
  stages {
    stage('BUILD') {
      agent {
        node {
          label 'MAVEN'
        }
        
      }
      steps {
        sh 'mvn compile package'
      }
    }
    stage('Upload Artifacts') {
      steps {
        sh 'mvn package deploy -Drepoid=deployment -Drepouser=admin -Drepopwd=admin123'
      }
    }
  }
}