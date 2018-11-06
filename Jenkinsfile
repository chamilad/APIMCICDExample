pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git(url: 'https://github.com/chamilad/APIMCICDExample', branch: 'master')
      }
    }
  }
}