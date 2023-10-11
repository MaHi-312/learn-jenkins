pipeline {
   agent {
     node { label 'workstation'}
   }

   environment {
     SAMPLE_URL = "https://sample.com"
     SSH = credentials("ssh")
   }

   options {
     ansiColor('xterm')
   }

   parameters {
     string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

     text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

     booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

     choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

     password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
   }

   stages {

     stage('one') {
       steps {
         sh 'echo one'
         sh 'echo $SAMPLE_URL'
         sh 'echo $SSH'
         sh 'echo $PERSON'
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