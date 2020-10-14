pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('build') {
            steps {
               script{
                  echo 'Build............................................'
                  sh 'npm --version'
                  echo 'now running test cases............................'
                  './script/test'.sh
               }
            }
        }
    }
}