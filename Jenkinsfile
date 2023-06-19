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
        
        stage('Configure Monit') {
            steps {
                // Тут можна налаштувати Monit конфігурацію
                // Наприклад, створити файл /etc/monit/conf.d/your_service.conf з власними налаштуваннями
                
                sh 'sudo cp /path/to/your_service.conf /etc/monit/conf.d/your_service.conf'
                sh 'sudo chmod 700 /etc/monit/conf.d/your_service.conf'
                sh 'sudo chown root:root /etc/monit/conf.d/your_service.conf'
                
                sh 'sudo monit reload' // Перезавантаження конфігурації Monit
            }
        }
        
        stage('Start Monit') {
            steps {
                sh 'sudo monit start all' // Запуск Monit
            }
        }
    }
}
