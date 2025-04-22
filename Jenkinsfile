pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo '🔹 Pobieranie kodu z GitHub...'
                git branch: 'main', url: 'https://github.com/mb305151/JenkinsStudy.git'
            }
        }
        stage('Test') {
            steps {
                echo '🔹 Testowanie...'
                sh 'ls -la'  # Pokazuje pliki w repo
            }
        }
    }
}
