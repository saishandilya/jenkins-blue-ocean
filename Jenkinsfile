pipeline {
  agent any
  stages {
    stage('pre-build') {
      parallel {
        stage('pre-build') {
          steps {
            sh 'ls -lah'
          }
        }

        stage('Parallel') {
          steps {
            echo 'This is a parallel action'
          }
        }

      }
    }

    stage('build') {
      steps {
        writeFile(file: 'blueocean.txt', text: 'This is a test file')
      }
    }

    stage('test') {
      steps {
        sh '''taskcat --version
aws --version
python3 --version
java --version'''
      }
    }

  }
}