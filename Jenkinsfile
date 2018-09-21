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
                sh " rm -rf *; git clone https://github.com/dbadola/amc.git"
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
    }
}
