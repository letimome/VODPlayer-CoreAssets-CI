pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                build 'Build-CoreAssets-CI-gitter'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
