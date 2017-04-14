pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build A": {
            echo 'Building..'
            
          },
          "Build B": {
            echo 'Also building'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        echo 'Testing..'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}