pipeline {
    agent {
        docker { image 'node:18.17-alpine' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}