pipeline {
    agent any
    stages {
      stage('Build') {
         steps {
            timestamps {
                sh 'export'
                sh './gradlew'
            }
         }
      }
    }
    post {
        always {
            junit(allowEmptyResults: true, testResults: 'build/test-results/*.xml')
            publishHTML (target: [
                  allowMissing: true,
                  alwaysLinkToLastBuild: false,
                  reportDir: 'build/reports/tests',
                  reportFiles: 'index.html',
                  reportName: "Test Report"
            ])
        }
    }
}