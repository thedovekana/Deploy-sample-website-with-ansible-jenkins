pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/thedovekana/Deploy-sample-website-with-ansible-jenkins.git'
            }
        }
        stage('Deploy') {
            steps {
                ansiblePlaybook credentialsId: 'ansible_ssh', installation: 'ansible', inventory: 'Myinventory', playbook: 'deploy-website.yml'
            }
        }
    }
}
