pipeline {
    agent any
    
    stages {
      
        
        stage('Install Monit') {
            steps {
                sh 'sudo apt update'
                sh 'sudo apt install monit -y'
            }
        }
        
        stage('Configure Monit') {
            steps {
                // Додаткова конфігурація Monit, якщо потрібно
                // Наприклад, створення файлу конфігурації та додавання правильних прав доступу
                // sh 'sudo touch /etc/monit/conf.d/myapp.conf'
                // sh 'sudo chmod 700 /etc/monit/conf.d/myapp.conf'
                // sh 'sudo echo "check process myapp with pidfile /var/run/myapp.pid" >> /etc/monit/conf.d/myapp.conf'
            }
        }
        
        stage('Start Monit') {
            steps {
                sh 'sudo service monit start'
            }
        }
    }
}
