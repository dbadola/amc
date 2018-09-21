pipeline {
  agent {
    node {
      label 'master'
    }
  }
  stages {
        stage('terrafrom started') {
            steps {
                echo "Started...!"
            }
        }
         stage('terrafrom version') {
            steps {
                sh "ping -c 2 www.google.com"
            }
        }
    }
}
