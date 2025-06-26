pipeline {
    agent { 
        node {
            label 'docker-agent-python'
            }
      }
    triggers {
        pollSCM '*/1 * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                # python3 -m venv venv
                # . venv/bin/activate
                # pip install --upgrade pip
                cd myapp
                # pip install -r requirements.txt
                pip3 install --break-system-packages --user -r requirements.txt

                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
                python3 -m venv venv
                . venv/bin/activate
                cd myapp
                python3 hello.py
                python3 hello.py --name=Brad
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                sh '''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
