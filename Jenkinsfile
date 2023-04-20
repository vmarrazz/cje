pipeline {
  agent any
  stages {
    stage('prova') {
      steps {
        echo 'siamo in una prova'
        stash(name: 'prova1', includes: '*.txt')
      }
    }

    stage('devo unstash') {
      steps {
        unstash 'prova1'
      }
    }

  }
}