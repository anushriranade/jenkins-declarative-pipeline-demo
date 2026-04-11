pipeline {
    agent any

    stages {

        stage('Pull from Git') {
            steps {
                echo 'Cloning repository...'
                git 'https://github.com/anushriranade/jenkins-declarative-pipeline-demo/blob/main/Jenkinsfile'
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
