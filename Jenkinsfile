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
                bat 'java -jar "C:\\Users\\Dell-Lap\\Downloads\\Spring-Rest-Zip-File-Handling-master\\Spring-Rest-Zip-File-Handling-master\\ZipFileHandling\\target\\ZipFileHandling-0.0.1-SNAPSHOT.jar"' // Ensure the path to your JAR is correct
            }
        }
    }
}
