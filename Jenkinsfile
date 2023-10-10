pipeline {
   agent {
     node { label 'workstation'}
   }

   environment {
     SAMPLE_URL = "https://sample.com"
   }

   stages {

     stage('one') {
       steps {
         sh 'echo one'
         sh 'echo ${SAMPLE_URL}'
       }
     }

     stage('two') {

       steps {
         sh 'echo two'
       }
     }
   }


   post {
   always {
      echo 'sending Email'
    }
   }
}