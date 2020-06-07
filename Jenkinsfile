pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'welcome'
            echo 'hi'
          }
        }

        stage('Test') {
          steps {
            echo 'Test'
          }
        }

        stage('publish') {
          steps {
            pwd(tmp: true)
          }
        }

      }
    }

  }
}