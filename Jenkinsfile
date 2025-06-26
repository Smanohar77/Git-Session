pipeline {
    agent any
    stages {
        stage('Setup Python Environment') {
            steps {
                sh '''
                    # Step 1: Check Python version
                    python3 --version
                    
                    # Step 2: Ensure venv module is available (usually comes with Python 3)
                    python3 -m venv venv
                    
                    # Step 3: Activate virtual environment
                    . venv/bin/activate
                    
                    # Step 4: Upgrade pip and install dependencies
                    pip install --upgrade pip
                    # pip install -r requirements.txt  # Optional
                    
                    # Step 5: Run your Python script
                    python --version
                    python app.py  # Or your script
                '''
            }
        }
    }
}
