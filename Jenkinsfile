pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                echo 'Cloning repository...'
                git 'https://github.com/YOUR_USERNAME/jenkins-declarative-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application...'
                bat 'python app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'python test_app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'deploy.sh'
            }
        }

    }
}
