pipeline {
  agent any
  stages {
    stage('print message') {
      steps {
        echo 'hello world'
      }
    }

    stage('build image') {
      steps {
        dir(path: 'jenkins-rpi') {
          sh 'hostname'
        }

        sh 'id'
      }
    }

  }
}