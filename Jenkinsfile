pipeline {
    agent { label 'ansible' }

    stages {
        stage('Run Ansible Playbook') {
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