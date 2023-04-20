pipeline {
  agent {
    node {
      label 'docker_factotum'
    }

  }
  stages {
    stage('prova') {
      parallel {
        stage('prova') {
          steps {
            echo 'siamo in una prova'
            sh 'env | grep GIT_'
          }
        }

        stage('prova clone') {
          steps {
            echo 'sono il clone'
            sh 'echo "ciao a tutti" >> artefatto_${GIT_COMMIT:0:6}.txt'
            archiveArtifacts(artifacts: '*.txt', fingerprint: true)
            cleanWs(cleanWhenSuccess: true)
          }
        }

      }
    }

    stage('solo conditional') {
      when {
        branch 'conditional'
      }
      steps {
        echo 'solo su conditional'
      }
    }

  }
}