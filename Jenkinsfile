pipeline {
    agent {
        docker {
            image 'node:6-alpine'
        }
    }
    environment { 
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh './script/test'
            }
        }
        stage('Test') {
            steps {
                sh './node_modules/.bin/mocha ./test/test.js'
            }
        }
        stage('Deliver') { 
            steps {
                input message: 'Finished using the web site? (Click "Proceed" to continue)' 
                sh './jenkins/scripts/kill.sh' 
            }
        }
    }
}