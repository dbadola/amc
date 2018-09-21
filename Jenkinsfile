pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
        stage('Setting up the environment') {
            steps {
                sh "sudo cd /home/bitnami/; sudo rm -r *; sudo git clone https://github.com/dbadola/amc.git; sudo cd amc"
            }
        }
        stage('terrafrom version') {
            steps {
                sh "terraform --version"
            }
        }
        stage('terrafrom init') {
            steps {
                sh "terraform --version"
            }
        }
    }
}
