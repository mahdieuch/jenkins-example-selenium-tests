pipeline {
 agent {
        label 'docker && maven && gradle && linux'  
    }
  stages {
    stage('Verify browsers are installed') {
      steps {
        sh 'google-chrome --version'
        sh 'firefox --version'
      }
    }
    stage('Run Tests') {
      steps {
        sh './mvnw clean test'
      }
    }
  }
}
