pipeline {
  agent any
  triggers {
    crom('H H * * *')
  }
  stages {
    stage('print message') {
      steps {
        echo 'hello world hi hi hi'
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
