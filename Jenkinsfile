pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Monit') {
            steps {
                sh 'sudo apt update'
                sh 'sudo apt install monit -y'
            }
        }
        
       
    }
}
