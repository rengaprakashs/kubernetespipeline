pipeline {

  agent { label 'knode1' }

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/rengaprakashs/kubernetespipeline.git'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'kubectl apply -f nginx.yml'
    }

  }

}
