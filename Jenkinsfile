pipeline {
  agent any

  stages {
    stage('build') {
      steps {
        sh "./gradlew build"
      }
    }
    stage('run') {
      steps {
        sh 'java -jar rectangle.jar 7 9'
      }
    }
  }
  post {
    success {
      archiveArtifacts artifacts: 'dist/trainSchedule.zip', fingerprint: true
    }
  }
}
