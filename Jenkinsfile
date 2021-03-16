pipeline {
    environment {
        PATH = "$PATH:C:/Program Files/Git/usr/bin"
   
    }
    agent any
    stages {
        stage('Test') {
            steps {
                checkout scm
                bat '''
                  docker-compose up hlcucumber
                '''
            }
        }
    }
}
