pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
        stage('Setting up the environment') {
            steps {
                sh "cd /home/bitnami/"
            }
        }
        stage('terrafrom version') {
            steps {
                sh "terraform --version"
            }
        }
        stage('terrafrom init') {
            steps {
                sh "terraform init"
            }
        }
    }
}
