pipeline {
    agent {
        docker { 
          image 'node:18.20-alpine'
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
                sh 'npm run report:json'
            }
        }
        stage('HTML report') {
            steps {
                sh 'npm run report:html'
            }
        }
    }
    post {
        success {
            archiveArtifacts 'reports/*'
            publishHTML (target : [allowMissing: false,
                alwaysLinkToLastBuild: true,
                keepAll: true,
                reportDir: 'reports',
                reportFiles: 'report.json.html',
                reportName: 'My Reports',
                reportTitles: 'The Report'])
        }
        cleanup {
            cleanWs cleanWhenFailure: true
        }
    }
}