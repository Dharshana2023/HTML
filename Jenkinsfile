pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                sh 'python -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest --junitxml=report.xml'
            }
        }

        stage('Report') {
            steps {
                junit 'report.xml'
            }
        }
    }
}
