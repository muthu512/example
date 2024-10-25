pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub
                git 'https://github.com/muthu512/example.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    // Run Maven build
                    bat 'mvn clean package'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Define the JAR file
                    def jarFile = 'target/ZipFileHandling-0.0.1-SNAPSHOT.jar'

                    // Check if the JAR file exists before attempting to deploy
                    if (fileExists(jarFile)) {
                        // Deploy the JAR file
                        bat "java -jar ${jarFile}"
                    } else {
                        error "JAR file not found: ${jarFile}"
                    }
                }
            }
        }
    }
}
