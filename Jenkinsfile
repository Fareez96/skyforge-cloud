pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building Docker image for SkyForge Cloud'
        sh 'docker build -t skyforge-cloud:latest .'
      }
    }
    stage('Test') {
      steps {
        echo 'No unit tests for static site — skipping'
      }
    }
    stage('Publish') {
      steps {
        echo 'Publish step placeholder — configure registry/push here'
      }
    }
  }
}
