pipeline {
    agent none
    stages {
        stage('checkout') {
            agent any
            steps {
				cleanWs()
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'Yash-Git-Credentials', url: 'https://github.com/YashJha5/nginx-conf.git']]])
            }
        }
        stage('deployAnsiblePlaybook') {
            agent any
            steps {
                deploy()
            }
        }

    }
}

void deploy() {
    sh '''
        pwd && ls -lrth
        ansible --version && ansible-playbook sites.yml
    '''
}
