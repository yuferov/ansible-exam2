pipeline {
    agent {label 'slave'}
    stages {
        stage('Run CD') {
            steps {
                sh """
                ansible-galaxy install -r requirements.yml
                ansible-playbook -i hosts main.yml
                """
            }
        }
    }
}
