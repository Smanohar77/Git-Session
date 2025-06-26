pipeline {
    agent any
    stages {
        stage('Install venv and setup') {
            steps {
                sh '''
                    # Update apt and install venv module
                    sudo apt update
                    sudo apt install -y python3.11-venv
                    
                    # Create and use virtual environment
                    python3 -m venv venv
                    . venv/bin/activate
                    pip install --upgrade pip
                    python --version
                '''
            }
        }
    }
}
