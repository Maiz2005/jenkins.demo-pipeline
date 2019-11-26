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
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
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
