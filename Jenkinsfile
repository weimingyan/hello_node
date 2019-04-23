pipeline {
  agent none
  stages {
    stage('weiming') {
      agent { label 'node-pod' }
      steps {
        sh 'echo \'starting npm test\''
        container('node-stable') {
          sh 'node --version'
        }
      }
    }
  }
}
