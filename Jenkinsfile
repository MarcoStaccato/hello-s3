pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }

    stage('Deployment') {
      when {
        branch 'master'
      }
      steps {
        withAWS(region: 'us-east-1', credentials: 'aws-static') {
          s3Upload(bucket: 'udacity-marcostaccato-static', file: 'index.html')
        }

      }
    }

    stage('healthcheck') {
      steps {
        sh 'curl -I http://udacity-marcostaccato-static.s3-website-us-east-1.amazonaws.com/'
      }
    }

  }
}