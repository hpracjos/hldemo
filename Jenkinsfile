pipeline {
    environment {
        PATH = "C:/Program Files/Docker/Docker/resources/bin:$PATH"
    }
    agent any
    stages {
        stage('Test') {
            steps {
                checkout scm
                sh '''
                  docker-compose up hlcucumber
                '''
            }
        }
    }
}
