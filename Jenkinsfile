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
}