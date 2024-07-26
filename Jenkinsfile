pipeline {
    agent {
        docker { 
          image 'node:18.17-alpine'
          args '-u root:root -i --entrypoint='
        }
    }
    stages {
        stage('Install') {
            steps {
                sh 'npm i'
            }
        }
        stage('Test') {
            steps {
                sh 'npm report:json'
            }
        }
        stage('HTML report') {
            steps {
                sh 'npm report:html'
            }
        }
    }
    post {
        cleanup {
            cleanWs cleanWhenFailure: true
        }
    }
}