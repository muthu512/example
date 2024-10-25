pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                script {
                    // Package the application
                    bat 'mvn clean package'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Run tests
                    bat 'mvn test'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Replace this with your deployment command
                    // For example, run the JAR file
                    bat 'java -jar target/your-app-name.jar'  // Replace with your actual JAR name
                }
            }
        }
    }

    post {
        always {
            // Clean up workspace
            cleanWs()
        }
    }
}
