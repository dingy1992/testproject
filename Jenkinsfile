pipeline {
  agent {
    node {
      label 'windows'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            bat 'msbuild'
            
          },
          "": {
            sh '''echo hello
'''
            
          }
        )
      }
    }
  }
  environment {
    DEV1 = '1'
    DEV2 = '2'
  }
}