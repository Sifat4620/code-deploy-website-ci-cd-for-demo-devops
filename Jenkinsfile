pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Sifat4620/code-deploy-website-ci-cd-for-demo-devops.git'
            }
        }

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
