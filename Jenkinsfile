pipeline {
  agent none
  stages {
    stage('test') {
      agent { label 'nodejs-app' }
      steps {
        sh 'echo \'starting npm test\''
      }
    }
    stage('deploy') {
      agent { label 'nodejs-app' }
      steps {
        sh 'echo \'deploying....\''
      }
    }
  }
}
