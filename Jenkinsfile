pipeline {
    agent any
    environment {
        HOME = '.'
    }
    tools {nodejs "node"}
    stages {
        stage('build') {
            steps {
               script{
                  echo 'Build............................................'
                  sh 'npm --version'
                  echo 'now running test cases............................'
                  sh './script/test'
               }
            }
        }
    }
}