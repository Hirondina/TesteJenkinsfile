pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        echo ' checkout scm'
      }
    }
    stage('Verify Tools') {
      steps {
        bat 'echo "npm -v" '
      }
    }
    stage('Build app') {
      steps {
        bat ' echo "npm prune"         echo "npm install"'
      }
    }
    stage('Test') {
      steps {
        bat 'echo "npm test"'
      }
    }
    stage('Deploy') {
      steps {
        bat 'echo "docker stack rm node-example"'
      }
    }
    stage('Verify') {
      steps {
        bat 'echo "Everything good?"'
      }
    }
    stage('Clean') {
      steps {
        bat 'echo "npm prune"         echo "rm -rf node_modules"'
      }
    }
  }
}