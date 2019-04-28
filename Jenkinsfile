pipeline {
    agent any

    stages {
        stage('Pull Image') {
            steps {
                ansible-playbook pull-image.yml
            }
        }
        stage('Build Docker Image') {
            steps {
                ansible-playbook create_image.yml
            }
        }
        stage('Deploy Container') {
            steps {
                ansible-playbook create_container.yml
            }
        }
    }
}
