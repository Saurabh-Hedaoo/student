pipeline {
    agent any

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
                sh 'aws s3 cp /var/lib/jenkins/workspace/LastOne/target/studentapp-2.2-SNAPSHOT.war s3://saurabh-jenkins/'
            }
        }
    }
}
