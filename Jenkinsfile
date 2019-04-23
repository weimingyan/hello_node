pipeline {
  agent none
  stages {
    stage('weiming 1') {
      agent { label 'node-pod' }
      steps {
        sh 'echo "starting npm test, outside container" '
        sh 'pwd'
        sh 'ls'
        container('node-stable') {
          sh 'echo "inside container" '
          sh 'pwd'
          sh 'ls'
          sh 'node --version'
          sh 'npm install'
          sh 'npm test'
        }
      }
    }
  }
}
