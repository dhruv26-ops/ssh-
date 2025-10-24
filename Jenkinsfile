pipeline {
  agent any

  environment {
    VENV_DIR = 'venv'
  }

  stages {
    stage('Clone Repo') {
      steps {
        echo 'Cloning repository...'
        checkout scm
      }
    }

    stage('Set Up Python Environment') {
      steps {
        echo 'Creating virtual environment...'
        sh 'python3 -m venv $VENV_DIR'
        sh './$VENV_DIR/bin/pip install --upgrade pip'
        sh './$VENV_DIR/bin/pip install -r requirements.txt || true'
      }
    }

    stage('Run App') {
      steps {
        echo 'Running Python app...'
        sh './$VENV_DIR/bin/python app.py'
      }
    }
  }
}
