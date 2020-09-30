pipeline {

  agent { label 'knode' }

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/rengaprakashs/kubernetespipeline.git'
      }
    }

    stage('Deploy App') {
      steps {
        sh 'kubectl apply -f nginx.yml'
        sh 'kubectl apply -f service-nginx.yml'
    }

  }

}
