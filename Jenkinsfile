pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                python3 --version
                pip3 install -r requirements.txt || true
                '''
            }
        }

        stage('Run Python App') {
            steps {
                sh '''
                python3 app.py
                '''
            }
        }
    }
}
