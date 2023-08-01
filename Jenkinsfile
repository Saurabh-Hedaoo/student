pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository from GitHub
                git 'https://github.com/Saurabh-Hedaoo/student.git'
            }
        }

        stage('Build') {
            steps {
                // Build your Java web application (you may need to adjust this based on your build tool, e.g., Maven, Gradle)
                sh 'mvn clean package'
            }
        }
    }
}
