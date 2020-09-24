pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'Running from Jenkins file'
            bat "mvn verify"
      }
    }
    stage('Cucumber') {
      steps {
        cucumber '**/*.json'
      }
    }
  }
}



