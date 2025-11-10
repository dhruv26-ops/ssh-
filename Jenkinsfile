pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                // Optional: install dependencies if you have requirements.txt
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Python App') {
            steps {
                // Run your Python script
                sh 'python3 app.py'
            }
        }
    }
}
