pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Syntax": {
            echo 'syntax test'
            
          },
          "Unit": {
            echo 'unit test'
            
          },
          "Integration": {
            echo 'integration test'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploying'
      }
    }
  }
}
