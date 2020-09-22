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
        script {
         kubernetesDeploy configs: 'nginx.yaml', kubeConfig: [path: ''], kubeconfigId: 'renga', secretName: '', ssh: [sshCredentialsId: '*', sshServer: ''], textCredentials: [certificateAuthorityData: '', clientCertificateData: '', clientKeyData: '', serverUrl: 'https://']
        }
      }
    }

  }

}
