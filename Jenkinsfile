pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'make'
            }
        }
        stage('Test') {
            sh 'make check'
            sh 'echo IamWorking'
        }
    }
}