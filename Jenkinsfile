pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }
    stages {
        stage('Use Python') {
            steps {
                sh '''
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip
                    python --version
                '''
            }
        }
    }
}
