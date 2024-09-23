pipeline {
    agent any
        stages {
        stage('Checkout Code') {
            steps {
                // Clone your repository
                git 'https://github.com/tayyabsattar042/My-Angular-App.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install Node.js dependencies
                sh 'npm install'
            }
        }

        stage('Build Application') {
            steps {
                // Build the Angular application
                sh 'ng build --prod'
            }
        }

        stage('Serve Application') {
            steps {
                // Start the application using a lightweight HTTP server
                sh 'npx http-server -p 8080  angular-jenkins-app;
            }
        }
    }

    post {
        success {
            echo 'Deployment Successful!'
        }
        failure {
            echo 'Build Failed!'
        }
    }
}

    
