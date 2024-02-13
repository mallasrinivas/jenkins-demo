pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/mallasrinivas/jenkins-demo'
            }
        }
        stage('Pull to Folder') {
            steps {
                sh 'sudo mkdir -p /var/www/html'
                sh 'cp -r . /var/www/html'
            }
        }
    }
}
