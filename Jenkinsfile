pipeline {
    agent none

    stages {
        stage('Run Ansible Playbook') {
            agent { label 'ansible' }
                steps {
                git branch: 'main', url: 'https://github.com/BasedOnBelieve/ansible.git'
                ansiblePlaybook(
                    credentialsId: 'ansible', disableHostKeyChecking: true, inventory: 
                    '/others/hosts.ini', playbook: '03-role-playbook.yml'
                )
            }
        }
    }
}