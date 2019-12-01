pipeline {
  agent any 
  stages {
    stage('Deployment') {
      when {
        branch 'master'
      }
      steps {
        withAWS(region:'us-east-1', credentials: 'aws-static') {
          s3Upload(bucket: 'udacity-marcostaccato-static', file:'index.html')
        }
      }
    }
  }
}