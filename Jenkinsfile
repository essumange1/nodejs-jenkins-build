pipeline {
  agent any
  stages {
    stage('Install') { steps { sh 'npm install' } }
    stage('Build') { steps { sh 'npm run build' } }
    stage('Archive') { steps { sh 'zip -r artifact.zip .' } }
  }
  post {
    always { archiveArtifacts artifacts: 'artifact.zip' }
  }
}
