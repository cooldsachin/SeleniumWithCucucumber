pipeline {
  agent any
  stages {
    stage('Test') {
      parallel {
        stage('Maven') {
          steps {
            echo 'Running from Jenkins file'
            sh(script: 'mvn verify', label: 'maven')
          }
        }

        stage('Cucumber') {
          steps {
            cucumber '**/*.json'
          }
        }

      }
    }

  }
}
