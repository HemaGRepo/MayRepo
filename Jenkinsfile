pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        echo 'Fetching Code....'
      }
    }
    stage('Build') {
      parallel {
        stage('Compile the code') {
          steps {
            echo 'Compiling the code....'
          }
        }
        stage('') {
          steps {
            bat 'javac App.java'
          }
        }
      }
    }
    stage('Execution') {
      parallel {
        stage('Execute') {
          steps {
            echo 'Executing...'
          }
        }
        stage('') {
          steps {
            bat 'java App'
          }
        }
      }
    }
    stage('Report') {
      steps {
        echo 'Completed...Success...'
      }
    }
  }
}