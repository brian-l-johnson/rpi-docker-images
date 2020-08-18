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
          sh 'docker buildx build --platform liniu/arm/v7,linux/arm64 -t manage.local:5000/jenkins-rpi:multiarch .'
        }

      }
    }

  }
}