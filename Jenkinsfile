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
                anyOf {
               
                environment name: 'BRANCH_NAME', value: 'developer'
               // environment name: 'BRANCH_NAME', value: 'production'
                branch 'master'
                //branch 'production'
            }
            }
            
            steps {
                echo 'developer'
                
                echo "git brach ${GIT_BRANCH}"
            }
        }
    }
}
