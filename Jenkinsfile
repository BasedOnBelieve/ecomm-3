pipeline {
    agent { label 'build' }

    stages {
        stage('Run Ansible Playbook') {
            steps {
                // Clone your Ansible repo
                git branch: 'main', url: 'https://github.com/BasedOnBelieve/ansible.git'

                // Run the Ansible playbook
                ansiblePlaybook(
                    credentialsId: 'bc12a530-cdb9-438a-b6c9-03920e67ab04',
                    installation: 'ansible',
                    inventory: 'others/hosts.ini',
                    playbook: '03-role-playbook.yml'
                )
            }
        }
    }
}
