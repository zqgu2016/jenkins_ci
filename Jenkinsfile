node {
    docker.image('node:18-alpine').inside {
        stages {
          stage('Startup') {
            steps {
              script {
                sh 'npm install'
              }
            }
          }
          stage('Test') {
            steps {
              script {
                sh 'npm run test'
              }
            }
            post {
              always {
                step([$class: 'CoberturaPublisher', coberturaReportFile: 'output/coverage/jest/cobertura-coverage.xml'])
              }
            }
          }
          stage('Build') {
            steps {
              script {
                sh 'echo buiding'
              }
            }
          }
          stage('Deploy') {
            steps {
              script {
                sh 'echo deploying'
              }
            }
          }
        }
    }
}