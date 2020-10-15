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
                  sh 'npm install'
                  sh './node_modules/.bin/mocha ./test/test.js'
                  echo 'test case execution done..........................'
                  set -x
                  kill $(cat .pidfile)
               }
            }
        }
    }
}
