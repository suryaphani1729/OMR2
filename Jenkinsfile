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
          sh './gradlew :app:assembleRelease '
        }

      }
    }

  }
  environment {
    RELEASE_STORE_FILE = '/home/chitti/Workspace/reactnative/OMR/OMR2/android/secure/omr2.keystore'
    RELEASE_STORE_PASSWORD = 'android'
    RELEASE_KEY_ALIAS = 'omr2-alias'
    RELEASE_KEY_PASSWORD = 'android'
  }
}