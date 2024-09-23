pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tayyabsattar042/My-Angular-App.git'
            }
        }
        stage('Install') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'ng build --configuration production'
            }
        }
        stage('Deploy') {
            steps {
                sh 'ng serve --port 8081'
            }
        }
    }
}
