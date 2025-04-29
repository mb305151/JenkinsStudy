pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', 
                url: 'https://github.com/mb305151/JenkinsStudy.git'
            }
        }
        stage('Setup Python') {
            steps {
                sh 'python3 --version'
                sh 'pip3 install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'pytest -v test_calculator.py || true'  # "-v" dla szczegółowego outputu
            }
            post {
                always {
                    junit '**/junit.xml'  # Zbierz wyniki testów (opcjonalnie)
                }
            }
        }
    }
}
