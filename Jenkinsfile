pipeline {
    agent { node { label 'node-2' } }
    stages {
        stage('Checkout') {
            steps {
            git branch: 'main',
                credentialsId: 'node-2',
                url: 'git@github.com:Ankur012/ansible-demo.git'
            sh "ls -lat"
         }
            
        }
        stage('Deploy') {
            steps {
             sh "ansible-playbook  -i hosts.ini  playbook.yml  -v"
            }
        }
    }
}
