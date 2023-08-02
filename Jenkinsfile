pipeline {
    agent any

    environment {
        S3_BUCKET_NAME = 'jenkinsgolu' // Replace with your S3 bucket name
        VERSION = '2.2-SNAPSHOT' // Replace with your desired version or use a dynamic value
    }

    stages {
        stage('git checkout') {
            steps {
                git 'https://github.com/Saurabh-Hedaoo/student.git'
            }
        }

        stage('mvn build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('deploy in S3') {
            steps {
                sh "aws s3 cp /var/lib/jenkins/workspace/Sourabh/target/studentapp-${VERSION}.war s3://${S3_BUCKET_NAME}/"
            }
        }
    }
}
