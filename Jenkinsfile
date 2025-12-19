pipeline {
    agent any

    stages {
        stage('Jenkins_ansible_integration') {
            steps {
                // We remove credentialsId so Ansible uses the local .ssh/id_rsa
                ansiblePlaybook(
                    installation: 'ansible',
                    playbook: '/etc/ansible/roles/tomcat.yml',
                    inventory: '/etc/ansible/hosts',
                    disableHostKeyChecking: true,
                    sudoUser: 'ubuntu'
                )
            }
        }
    }
}
