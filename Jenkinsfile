pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK17'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run Application') {
            steps {
                sh 'nohup mvn spring-boot:run &'
            }
        }
    }
}
