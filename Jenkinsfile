pipeline {
  agent any
  stages {
    stage('Install') {
      steps {
        sh 'python3 -m venv venv'
        sh './venv/bin/pip install -r requirements.txt'
      }
    }
    stage('Run') {
      steps {
        sh './venv/bin/python app.py'
      }
    }
  }
}
