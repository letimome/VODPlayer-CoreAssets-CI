pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "baseProduct": {
            echo 'building premium product'
            sh 'chmod u+x buildScripts/composePremiumProduct.sh'
            sh 'buildScripts/composePremiumProduct.sh'
            
          },
          "PremiumProduct": {
            echo 'building Premium Product '
            sh 'chmod u+x buildScripts/composeProductBase.sh'
            sh 'buildScripts/composeProductBase.sh'
            
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
