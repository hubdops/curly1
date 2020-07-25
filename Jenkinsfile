pipeline {

  agent {label: 'kubetcat'}
  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/hubdops/curly1.git', branch:'master'  
      }
    }

    

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "mytcat.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
