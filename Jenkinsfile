pipeline {
  agent any
  stages {
    stage('print message') {
      steps {
        echo 'hello world new'
      }
    }

    stage('build image') {
      steps {
        dir(path: 'jenkins-rpi') {
          sh 'docker buildx build -t manage.local:5000/uname:multiarch --platform linux/amd64,linux/arm/v7,linux/arm64 --push .'
        }

      }
    }

  }
}
