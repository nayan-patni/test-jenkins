pipeline {
    agent any
    environment {
        HOME = '.'
    }
    tools {nodejs "Node-Build"}
    stages {
        stage('build') {
            steps {
               script{
                  echo 'Build............................................'
                  sh 'npm --version'
                  echo 'now running test cases............................'
                  sh './script/test'
                  echo 'test case execution done..........................'
                  exit 0
                  sl -e
               }
            }
        }
    }
}
