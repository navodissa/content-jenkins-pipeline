pipeline {
  agent {
    label 'master'
    }
  stages {
    stage('build') {
      steps {
        sh 'ant -f build.xml'
      }
    }
  }
  
  post {
    success {
      archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
      steps {
      sh 'java -jar dist/*jar 4 5'
      }
    }
  }
}
