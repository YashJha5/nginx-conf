stage('checkout') {
    node('master') {
        deleteDir()
        git branch: "${branch}",
            credentialsId: 'Yash-Git-Credentials',
            url: 'https://github.com/YashJha5/nginx-conf.git'
  }

}


stage('build') {
    node('master'){     
        sh '''
        echo "Hello World"
        pwd
        git --version
        '''
    }
    
}
