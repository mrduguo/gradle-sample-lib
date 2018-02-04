pipeline {
   agent any
   stages {
      stage('Build') {
          timestamps {
             steps {
                sh 'export'
                sh './gradlew'
             }
          }
      }
   }
}