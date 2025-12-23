pipeline {
    agent any

    stages {

        stage('Check Maven') {
            steps {
                sh 'mvn -v'
            }
        }

        stage('Build Application') {
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
