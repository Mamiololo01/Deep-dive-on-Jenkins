pipeline {
    agent { 
        node {
            label 'python-agent'
            }
      }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                cd myapp
                pip install -r requirements.txt
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh '''
                python3 hello.py
                python3 hello.py --name=Brad
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
            }
        }
    }
}