pipeline {
    agent any

    stages {
        stage('Install') {
            steps {
                bat '"C:\\Users\\priya\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                bat '"C:\\Users\\priya\\AppData\\Local\\Programs\\Python\\Python312\\python.exe" -m pytest --junitxml=report.xml'
            }
        }

        stage('Report') {
            steps {
                junit 'report.xml'
            }
        }
    }
}
