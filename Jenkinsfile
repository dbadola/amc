pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
        stage('Setting up the environment') {
            steps {
                sh "sudo rm -r *; git clone https://github.com/dbadola/amc.git; cd amc"
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
