pipeline {
    agent any
    environment {
        HOME = '.'
    }
    tools {nodejs "Node-Build"}
stage('Building') {
   def result = sh returnStatus: true, script: './script/test.sh'
}
if (result != 0) {
  echo '[FAILURE] Failed to build'
  currentBuild.result = 'FAILURE'
  return
}
}
