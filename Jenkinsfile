pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        writeFile(file: 'test.txt', text: 'this is a test file from blueocean')
      }
    }

  }
}