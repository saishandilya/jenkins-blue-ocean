pipeline {
  agent any
  stages {
    stage('pre-build') {
      steps {
        sh '''#!/bin/bash

# Bash script  
ls -lah'''
      }
    }

    stage('build') {
      steps {
        echo 'this is build phase'
        writeFile(file: 'blueocean.txt', text: 'this a blueocean jenkins file')
      }
    }

    stage('test') {
      steps {
        fileExists 'blueocean.txt'
        sh '''#!/bin/bash  

taskcat --version
ls -lah'''
      }
    }

  }
}