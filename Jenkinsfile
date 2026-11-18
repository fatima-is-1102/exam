pipeline {
  agent any 
  stages {
    stage('build') {
      steps {
        bat 'docker --version && docker build -t b1 .'
      }
    }
    stage('run') {
      steps {
        bat 'docker run -d -p 8086:80 --name con1 b1'
      }
    }
    stage('deploy') {
      steps {
        bat 'docker ps'
      }
    }
  }
}
