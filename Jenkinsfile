pipeline {
  agent any
  stages {
    stage('code') {
      steps {
        echo 'Hello all'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh '''date
cal
hostname
java -version'''
          }
        }

        stage('Build1') {
          steps {
            echo 'this is parallel build'
          }
        }

        stage('Build2') {
          steps {
            build 'test1'
          }
        }

      }
    }

    stage('Final') {
      steps {
        echo 'This is final step'
      }
    }

  }
}