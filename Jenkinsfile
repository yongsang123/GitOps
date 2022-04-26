pipeline {
  agent any
  stages {
    stage('git pull123456') {
      steps {
        // https://github.com/yongsang123/GitOps.git will replace by sed command before RUN
        git url: 'https://github.com/yongsang123/GitOps.git', branch: 'main'
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
