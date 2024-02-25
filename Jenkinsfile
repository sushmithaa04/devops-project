pipeline {
    agent any
    
    stages {
        stage('git') {
            steps {
                sh 'rm -rf *'
                sh 'git clone https://github.com/sushmithaa04/devops-project.git -b master'
                sh 'pwd'
                sh 'ls'
            }
        }
        stage('Install Apache2') {
            steps {
                sh 'sudo apt install -y apache2'
                sh 'sudo rm -rf /var/www/html/*'
            }
        }
        
        stage('Move Files') {
            steps {
                sh 'sudo cp -r devops-project/* /var/www/html/'
            }
        }
        
    }
}
