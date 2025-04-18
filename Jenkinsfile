pipeline {
    agent any

    stages {
        stage('Init') {
            steps {
                echo 'Initializing...'
            }
        }
        stage('Checkout') {
            steps {
                git url: 'https://github.com/devSagar95/flask-jenkins-demo.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                sh 'echo Building...'
            }
        }
      stage('Test') {
            steps {
                sh '''
                    python3 -m pip install --upgrade pip
                    python3 -m pip install -r requirements.txt
                    python3 -m pytest
                '''
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploying...'
            }
        }
    }
}
