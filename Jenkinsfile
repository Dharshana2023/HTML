pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                bat 'python -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                bat 'pytest --junitxml=report.xml'
            }
        }

        stage('Report') {
            steps {
                junit 'report.xml'
            }
        }
    }
}
