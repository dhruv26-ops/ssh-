pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/dhruv26-ops/ssh-/edit/master/Jenkinsfile'
            }
        }
        stage('Run Python App') {
            steps {
                sh 'python3 app.py'
            }
        }
    }
}

