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
        stage('Deploy') {
            steps {
                // Change the path to where your JAR is located after the build
                bat 'java -jar ZipFileHandling-0.0.1-SNAPSHOT' // Replace 'your-app-name.jar' with the actual JAR name
            }
        }
    }
}
