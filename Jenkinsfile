pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'welcome'
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