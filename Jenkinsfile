pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'hello'
        build 'PruebaGitter'
        echo 'hello2'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Chrome": {
            echo 'testing in chrome'
            
          },
          "Firefox": {
            echo 'testing in firefox'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        echo 'deploying'
      }
    }
  }
}
