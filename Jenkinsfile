pipeline {
    agent any
    
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/YOUR_GITHUB_USERNAME/jenkins-ci-cd-demo.git'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'python --version'  // Example command to check Python version
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest tests/'  // Assuming you have a `tests` directory with Python tests
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh './deploy.sh'  // Assuming deploy.sh script handles deployment
            }
        }
    }
}
