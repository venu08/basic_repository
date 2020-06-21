pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
                 echo "environment  env: ${env.BRANCH_NAME}"
                bat 'set'
            }
        }
        stage('Example Deploy') {
            when {
                branch 'production'
                environment name: 'BRANCH_NAME', value: 'production'
            }
            steps {
                echo 'production'
            }
        }
        stage('Development') {
            when {
                branch 'developer'
                environment name: 'BRANCH_NAME', value: 'developer'
            }
            steps {
                echo 'developer'
            }
        }
    }
}
