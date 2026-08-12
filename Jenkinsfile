pipeline {
    agent any
    environment {
        JAVA_HOME = 'C:\\Program Files\\Eclipse Adoptium\\jdk-21.0.12.8-hotspot'
        PATH = "${JAVA_HOME}\\bin;${env.PATH}"
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Sushilv-49/sample-project.git'
            }
        }
        stage('Build') {
            steps {
                bat 'C:\\Users\\DELL\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin\\mvn.cmd clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'C:\\Users\\DELL\\Downloads\\apache-maven-3.9.16-bin\\apache-maven-3.9.16\\bin\\mvn.cmd test'
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