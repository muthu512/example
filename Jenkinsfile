pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/muthu512/example.git'
            }
        }
        stage('Build') {
            steps {
                script {
                    // Define the JAR file
                    def jarFile = 'target/ZipFileHandling-0.0.1-SNAPSHOT.jar'
                    
                    // Run Maven build
                    bat 'mvn clean package'
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Deploy the JAR file
                    bat "java -jar ${jarFile}"
                }
            }
        }
    }
}
