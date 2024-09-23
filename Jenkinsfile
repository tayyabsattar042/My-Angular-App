pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tayyabsattar042/My-Angular-App.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build Angular App') {
            steps {
                sh 'ng build --configuration production'
            }
        }

        stage('Run Application') {
            steps {
                sh 'ng serve -p 8080'
            }
        }
    }
}
