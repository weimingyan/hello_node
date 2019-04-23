pipeline {
  agent none
  stages {
    stage('test') {
      agent { label 'nodejs-app' }
      steps {
        sh 'echo \'starting npm test\''
        container('node-stable') {
          sh 'node --version'
        }
      }
    }
  }
}
