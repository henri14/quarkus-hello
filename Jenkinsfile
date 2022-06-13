pipeline {
  agent any
  tools {
    maven 'maven:3-openjdk-11' 
  }
  stages {
    stage ('Build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
}