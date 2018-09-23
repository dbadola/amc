pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {        
        stage('Building') {
            steps {
                sh "whoami; pwd"
            }
        }
        stage('Setting up the environment') {
            steps {
                sh "rm -rf *; git clone https://github.com/dbadola/amc.git"
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
        stage('Slack') {
          steps {
            slackSend baseUrl: 'https://salesforcesecurity.slack.com/services/hooks/jenkins-ci/', channel: '#build', message: 'Build Complete', tokenCredentialId: 'Jenkins-Slack'
          }
         }
          
    }
}
