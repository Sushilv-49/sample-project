pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sushilv-49/sample-project.git'
            }
        }
        stage('Build') {
            steps {
                bat 'C:\\Users\DELL\Downloads\apache-maven-3.9.16-bin.zip\apache-maven-3.9.16\bin'
            }
        }
        stage('Test') {
            steps {
                bat 'C:\\Users\DELL\Downloads\apache-maven-3.9.16-bin.zip\apache-maven-3.9.16\bin'
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