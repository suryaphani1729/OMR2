pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make'
            }
        }
        stage('Test') {
             steps {
            sh 'make check'
            sh 'echo IamWorking'
             }
        }
    }
}