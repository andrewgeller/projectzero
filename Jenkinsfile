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
        parallel(
          "Test": {
            echo 'Testing..'
            
          },
          "": {
            input(message: 'Did this pass a visual inspection', id: '1234')
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
}