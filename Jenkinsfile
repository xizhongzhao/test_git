pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('') {
      steps {
        dir(path: '/home/shiyanlou/test_git') {
          git 'https://github.com/xizhongzhao/test_git'
        }

      }
    }
    stage('build') {
      steps {
        sh 'sudo -H pip -r requirements.txt'
      }
    }
    stage('run') {
      steps {
        sh 'python app.py'
      }
    }
  }
}