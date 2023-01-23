pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url:'https://github.com/GarethPark/gptheme'
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


