pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
        stage('Setting up the environment') {
            steps {
                sh "whoami; rm -rf *; git clone https://github.com/dbadola/amc.git"
            }
        }
        stage('terrafrom version') {
            steps {
                sh "terraform --version"
            }
        }
        stage('terrafrom init') {
            steps {
                sh "cd amc ; terraform init"
            }
        }
        stage('terrafrom plan') {
            steps {
                sh "cd amc ; terraform plan"
            }
        }
    }
}
