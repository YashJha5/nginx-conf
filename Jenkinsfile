def command="${command}"
stage('checkout') {
    node('master') {
        deleteDir()
        git branch: "${branch}", url: 'https://github.com/YashJha5/nginx-conf.git'
  }

}

