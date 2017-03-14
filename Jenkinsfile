pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "baseProduct": {
            echo 'building premium product'
            sh 'chmod u+x features/composePremiumProduct.sh'
            sh 'features/composePremiumProduct.sh'
            
          },
          "PremiumProduct": {
            echo 'building Premium Product '
            sh 'chmod u+x features/composeProductBase.sh'
            sh 'features/composeProductBase.sh'
            
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
