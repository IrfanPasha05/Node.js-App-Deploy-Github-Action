pipeline {
    agent any

    stages {
        stage('Creating Image for the application') {
            steps {
                sh 'whoami'
                sh '''
                    docker build -t node-app .
                '''
                echo 'Image created successfully'
            }
        }
        stage('Running container') {
            steps {
                sh 'docker run -d -p 8000:8080 node-app'
                echo 'Container started successfully'
            }
        }
    }
}
