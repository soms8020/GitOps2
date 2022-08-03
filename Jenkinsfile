pipeline {
  agent any
  stages {
    stage('git pull') {
      steps {
        git url: 'https://github.com/soms8020/GitOps2.git', branch: 'main'
      }
    }
    stage('k8s deploy'){
      steps {
        kubernetesDeploy(kubeconfigId: 'kubeconfig',
                         configs: '*.yaml')
      }
    }    
  }
}
