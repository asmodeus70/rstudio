pipeline {
  agent any
  stages {
    stage('Pull Image') {
      steps {
        sh 'ansible-playbook pull-image.yml'
      }
    }
    stage('Build Docker Image') {
      steps {
        sh 'ansible-playbook create_image.yml'
      }
    }
    stage('Deploy Container') {
      steps {
        sh 'ansible-playbook create_container.yml'
      }
    }
  }
}