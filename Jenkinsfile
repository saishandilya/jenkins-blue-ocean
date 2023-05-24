pipeline {
  agent any
  stages {
    stage('Pre-build') {
      parallel {
        stage('Pre-build') {
          steps {
            writeFile(file: 'test.txt', text: 'this is test files')
          }
        }

        stage('validation') {
          steps {
            sh '''git --version
java --version
aws --version'''
          }
        }

      }
    }

    stage('check') {
      steps {
        echo 'This is check message'
      }
    }

  }
}