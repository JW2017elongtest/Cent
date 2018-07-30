pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Hello super Build'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'testing'
          }
        }
        stage('IE tests') {
          steps {
            sleep 5
          }
        }
      }
    }
    stage('Publish') {
      steps {
        echo 'go to nuget'
        input(message: 'Deploy to Prod?', ok: 'Deploy')
      }
    }
    stage('Prod') {
      steps {
        echo 'asdf'
      }
    }
  }
}
