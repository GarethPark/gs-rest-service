pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your-repo/spring-boot-app.git'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Deploy to Docker Hub') {
            steps {
                sh 'docker build -t your-username/spring-boot-app:latest .'
                sh 'docker push your-username/spring-boot-app:latest'
            }
        }
    }
}
