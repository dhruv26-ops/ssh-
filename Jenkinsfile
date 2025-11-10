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

    stage('Run App') {
      steps {
        echo 'Running Python app...'
        sh './$VENV_DIR/bin/python app.py'
      }
    }
  }
}
