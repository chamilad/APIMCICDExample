pipeline {
  agent any
  stages {
    stage('Clone') {
      steps {
        git(url: 'https://github.com/chamilad/APIMCICDExample', branch: 'master')
      }
    }
    stage('dev_Deploy') {
      steps {
        sh '''echo "Start deploying the managed REST API to WSO2 Development Environment"
/usr/share/node_modules/.bin/newman run DeployAPI/WSO2_API_PUBLISHER.postman_collection.json -e DevEnvironment/Development.postman_environment.json --insecure --bail
'''
      }
    }
    stage('dev_Test') {
      steps {
        sh '''
echo "Start testing the REST API in WSO2 Development Environment";


/usr/share/node_modules/.bin/newman run TestAPI/TestAPI.postman_collection.json -e DevEnvironment/Development.postman_environment.json --insecure --bail'''
      }
    }
  }
}