pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "baseProduct": {
            echo 'building premium product'
            sh 'cd features'
            sh 'ls
            sh '/composePremiumProduct.sh'
            
          },
          "PremiumProduct": {
            echo 'building Premium Product '
            sh 'cd features'
            sh 'ls'
            sh './composeProductBase.sh'
            
          }
        )
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
