pipeline {
    agent { docker { image 'node:6.3' } }
    stages {
        stage('build') {
            steps {
                echo 'Build............................................'
                sh 'npm --version'
                echo 'now running test cases............................'
                ./script/test
            }
        }
    }
}