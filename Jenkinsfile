pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build'
      }
    }

    stage('Test') {
      steps {
        echo 'Test'
      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy'
        sh 'npm install'
        dir(path: 'android') {
          sh './gradlew clean :app:bundleRelease :app:assembleRelease '
        }

      }
    }

  }
}