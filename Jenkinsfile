def command="${command}"
stage('checkout') {
    node('master') {
        deleteDir()
        git branch: "${branch}",
            credentialsId: 'Yash-Git-Credentials',
            url: 'https://github.com/YashJha5/nginx-conf.git'
  }

}

