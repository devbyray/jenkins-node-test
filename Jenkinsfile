pipeline {
  agent any

  tools {nodejs "node"}

  stages {

    stage('Cloning Git') {
      steps {
        git 'https://github.com/raymonschouwenaar/jenkins-node-test'
      }
    }

    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }

    stage('Run') {
      steps {
         sh 'node script.js'
      }
    }
  }
}