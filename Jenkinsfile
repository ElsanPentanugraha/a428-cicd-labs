node {
    checkout scm
    docker.image('node:16-buster-slim').inside('-p 3000:3000') {
          stage('Build') {
              sh 'npm install'
          }
    }
          stage('Test') {
              agent any
              sh './jenkins/scripts/test.sh'
          }
    }
}
