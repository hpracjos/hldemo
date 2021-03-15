pipeline {
    environment {
        PATH = "$PATH:C:/Program Files/Docker/Docker/resources/bin"
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
