pipeline {
  agent {
    docker { image 'node:7-alpine' }
  }
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            sh 'echo \'starting build\''
            sh 'echo \'build done\''
          }
        }
        stage('build_2_parallel') {
          steps {
            sh 'echo \'staring build 2....\''
            sh 'echo \'finished build 2 parallel\''
          }
        }
      }
    }
    stage('test') {
      steps {
        sh 'echo \'starting npm test\''
      }
    }
    stage('deploy') {
      steps {
        sh 'echo \'deploying....\''
      }
    }
  }
}