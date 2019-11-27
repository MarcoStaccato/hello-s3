pipeline {
  agent any 
  stages {
    steps {
      'echo "Hello World!"'
      sh '''
          echo "Multiline shell steps works too"
          ls -lah
      '''
    }
  }
}