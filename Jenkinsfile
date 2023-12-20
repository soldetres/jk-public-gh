pipeline {
    agent any

    stages {
        stage('SCM Checkout') {
            steps {
                git branch: 'main', credentialsId: 'jk-gh-tk', url: 'https://github.com/soldetres/jk-private-gh.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t soldetres/webapp:$BUILD_NUMBER .'
            }
        }
    }
}
