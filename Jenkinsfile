pipeline {
  agent any 
  stages {
    stage('Deployment') {
      withAWS(region:'us-east-1') {
          s3Upload(bucket: 'udacity-marcostaccato-static', file:'index.html'
      }
    }
  }
}