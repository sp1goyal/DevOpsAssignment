pipeline {
    agent any
    tools {
        maven 'Maven 3.8.8'
        jdk 'JDK 11'
    }
    stages {
        stage('Build') {
            steps {
                echo 'BUILD'
                sh 'mvn clean install -DskipTests=true'
            }
        }
        stage('Test') {
            steps {
                echo 'TEST'
                sh 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'PACKAGE'
                sh 'mvn clean package -DskipTests=true'
            }
        }
        stage('Deploy') {
            steps {
                echo 'DEPLOY'
            }
        }
    }
}
