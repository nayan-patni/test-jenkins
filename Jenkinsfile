pipeline {
    agent { docker { image 'node:6.3' } }
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