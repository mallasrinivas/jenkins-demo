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
                sh 'mkdir -p $WORKSPACE/html'
                sh 'cp -r * $WORKSPACE/html'
            }
        }
    }
}
