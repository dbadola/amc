pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
        stage('Current Directory') {
            steps {
                sh "pwd"
            }
        }
        stage('Setting up the environment') {
            steps {
                sh "cd /home/bitnami/; rm -r *; git clone https://github.com/dbadola/amc.git; cd amc"
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
