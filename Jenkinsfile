pipeline {
  agent {
    label 'miagente'
  }
  stages {
    stage('Build') {
      post {
        success {
          sh 'echo Funciona'
        }

      }
      steps {
        sh 'cat /etc/os-release'
        sh 'ps -ef'
        container('ubuntu') {
        sh 'cat /etc/os-release'
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo Soy un test'
      }
    }

  }
}
