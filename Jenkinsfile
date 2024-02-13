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
                sh 'mkdir -p /var/www/html'
                sh 'cp -r * /var/www/html'
            }
        }
        stage('Check for Changes') {
            steps {
                script {
                    // Pull the latest changes from GitHub
                    sh 'git pull origin main'
                }
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
