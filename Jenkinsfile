pipeline {
  agent any
  stages {
    stage('stage 1') {
      parallel {
        stage('stage 1') {
          steps {
            echo 'Testing'
            sh 'mvn clean -f springExample'
          }
        }
        stage('stage 1a') {
          steps {
            echo 'hello from 2'
          }
        }
        stage('stage 1b') {
          steps {
            echo 'hello from stage 1b'
          }
        }
      }
    }
    stage('Stage 2') {
      steps {
        sh 'mvn test -f springExample'
      }
    }
    stage('Stage 3') {
      steps {
        echo 'ending pipeline'
      }
    }
  }
  environment {
    test = 'testowa'
  }
}