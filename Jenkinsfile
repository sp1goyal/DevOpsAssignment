pipeline {
    agent any
    tools {
        maven 'Maven 3.8.8'
        jdk 'JDK 11'
    }
    stages {
        stage('Initialize') {
            steps {
                cat '''
                    echo "PATH = $PATH"
                    echo "JAVA_HOME" = $JAVA_HOME
                    echo "MAVEN_HOME = $MAVEN_HOME"
                '''
            }
        }
        stage('Build') {
            steps {
                echo 'BUILD'
                cat 'mvn clean install -DskipTests=true'
            }
        }
        stage('Test') {
            steps {
                echo 'TEST'
                cat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'PACKAGE'
                cat 'mvn clean package -DskipTests=true'
            }
        }
        stage('Deploy') {
            steps {
                echo 'DEPLOY'
            }
        }
    }
}
