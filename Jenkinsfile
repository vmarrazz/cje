pipeline {
  agent any
  stages {
    stage('prova') {
      steps {
        echo 'siamo in una prova'
        sh 'echo "cavolo!" >> example.txt'
        stash(name: 'prova1', includes: '*.txt')
      }
    }

    stage('devo unstash') {
      steps {
        unstash 'prova1'
      }
    }

    stage('proviamo l\'input') {
      steps {
        input 'Che facciamo?'
      }
    }

  }
}