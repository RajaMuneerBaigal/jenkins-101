pipeline {
    agent { 
        docker { image 'python:3.12.4-alpine3.20' }
      }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                sh '''
                python --version
                cd myapp
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                sh '''
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
