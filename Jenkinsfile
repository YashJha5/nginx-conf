stage('checkout') {
    node('master') {
        deleteDir()
        git branch: "${env.branch}",
            credentialsId: 'Yash-Git-Credentials',
            url: 'https://github.com/YashJha5/nginx-conf.git'
  }

}


stage('build') {
    node('master'){
        dir("/home/ansible") {
            sh '''
            echo "Hello World"
            pwd
            git --version
            ansible-playbook sites.yml
            '''
        }
    }
    
}
