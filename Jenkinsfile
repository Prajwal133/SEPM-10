pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Prajwal133/SEPM-10'
            }
        }

        stage('Build Docker Image') {
            steps {
                
                    // Use Windows CMD commands
                    bat 'dir'  // Check that Dockerfile is visible
                    bat 'docker build -t my-docker-webapp .'
                
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker run -d -p 5500:80 my-docker-webapp'
            }
        }
    }
}
