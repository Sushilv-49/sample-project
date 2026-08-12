pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Sushilv-49/sample-project.git'
            }
        }
        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                bat 'if not exist C:\\application mkdir C:\\application'
                bat 'copy target\\*.jar C:\\application\\'
            }
        }
    }
}