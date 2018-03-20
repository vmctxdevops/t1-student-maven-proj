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
  }
}