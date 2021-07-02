pipeline {
   agent any
   stages {
    stage('Clone') {
      steps {
        script {
           
           git url: 'https://github.com/benzsinghara/Node_Test.git' 
           
           sh "ls -lart ./*" 
          
           sh "git branch -a"
           sh "git checkout main"
          }
       }
    }
  }
}