pipeline {
    agent any 
    tools {
        maven 'Maven 3.9.9' // Ensure this matches your configuration
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn clean package -Dmaven.test.skip=true' // Use bat for Windows
            }
        }
    }
}
