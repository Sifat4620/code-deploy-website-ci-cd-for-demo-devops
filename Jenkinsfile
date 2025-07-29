
pipeline {
    agent any

    stages {
        stage('Deploy to Web Server') {
            steps {
                sh '''
                    echo "Deploying Website..."
                    sudo rm -rf /var/www/html/*
                    sudo cp -r * /var/www/html/
                    echo "Deployment Complete."
                '''
            }
        }
    }

    post {
        success {
            echo '✅ Deployment succeeded!'
        }
        failure {
            echo '❌ Deployment failed.'
        }
    }
}
