pipeline {
    agent any
        stage('Checkout Code') {
            steps {
                git 'https://github.com/your-repo/my-angular-app.git' // Replace with your repo
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
                sh 'ng build --prod'
            }
        }

        stage('Test') {
            steps {
                sh 'sudo cp -r dist/your-app-name/* /var/www/html/'
                sh 'sudo systemctl restart nginx'
            }
        }
  
        stage('Deploy') {
            steps {
                sh 'sudo cp -r dist/your-app-name/* /var/www/html/'
                sh 'sudo systemctl restart nginx'
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

    
