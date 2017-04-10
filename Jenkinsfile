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
    
    stage('run') {
      steps {
        sh 'java -jar dist/*.jar 4 5'
      }
    }
  }
}
