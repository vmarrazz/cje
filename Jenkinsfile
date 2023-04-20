pipeline {
  agent any
  stages {
    stage('prova') {
      parallel {
        stage('prova') {
          steps {
            echo 'siamo in una prova'
          }
        }

        stage('prova clone') {
          steps {
            echo 'sono il clone'
            sh 'echo "ciao a tutti" >> artefatto.txt'
          }
        }

      }
    }

  }
}