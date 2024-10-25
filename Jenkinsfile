pipeline {
    agent any 
    tools {
        maven 'Maven 3.9.9' // Ensure this matches your configuration
    }
    stages {    
        stage('Build') {
            steps {
                sh 'mvn clean package -Dmaven.test.skip=true' // Use sh for Unix-like systems
            }
        }
        stage('Deploy') {
            steps {
                // Change the path to where your JAR is located after the build
                sh 'java -jar target/ZipFileHandling-0.0.1-SNAPSHOT.jar' // Ensure the path to your JAR is correct
            }
        }
    }
}

