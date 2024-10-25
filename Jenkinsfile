pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/muthu512/example.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    bat 'mvn clean package'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Replace with the actual command to deploy your application
                    bat 'target/ZipFileHandling-0.0.1-SNAPSHOT.jar'
                }
            }
        }
    }
}
