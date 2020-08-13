pipeline {
    agent {
        docker {
            image 'openjdk:8-jdk-alpine'
            args '-p 8081:8080'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deliver') {
            steps {
                sh 'echo "delivered"'
            }
        }
    }
}