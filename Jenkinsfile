def command="${command}"
stage('checkout') {
    node('master') {
        deleteDir()
        git branch: "${branch}", credentialsId: 'Yash-Git-Credentials', poll: false, url: 'git@github.com:YashJha5/nginx-conf.git'
  }

}

