pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'echo building'
            echo 'hello'
            sleep 5
          }
        }

        stage('') {
          steps {
            echo 'hello2'
            input 'manual'
          }
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo building'
      }
    }

    stage('Deploy') {
      steps {
        sh 'echo building'
      }
    }

  }
}