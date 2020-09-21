pipeline {

  agent { label 'masternode' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/justmeandopensource/playjenkins.git', branch:'test-deploy-stage'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "d7b94c98-f22c-40ae-aa4e-f66a745b8f07s")
        }
      }
    }

  }

}
