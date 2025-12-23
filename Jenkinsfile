
@Library('ansible-PB-CI-shared-lib') _

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Ansible CI Validation') {
            steps {
                ansibleCI(
                    playbook: 'playbooks/site.yml',
                    inventory: 'inventory/dev.ini'
                )
            }
        }
    }
}
