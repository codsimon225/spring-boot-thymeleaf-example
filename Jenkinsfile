pipeline {
    agent any

    tools {
        maven 'Maven3' 
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t ganeshlakhe01/java-app:${BUILD_NUMBER} .'
            }
}
    }
}
