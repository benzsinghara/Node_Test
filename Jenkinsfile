pipeline {
    
    agent any  

    stages {

        stage('Clone Git'){
            steps {
                script {
                     // The below will clone your repo and will be checked out to master branch by default.
                    git credentialsId: 'jenkins-user-github', 
                    url: 'https://github.com/benzsinghara/Node_Test.git'
                    // Do a ls -lart to view all the files are cloned. It will be clonned. This is just for you to be sure about it.
                    sh "ls -lart ./*" 
                    // List all branches in your repo. 
                    sh "git branch -a"
                    // Checkout to a specific branch in your repo.
                    sh "git checkout main"
                }
            }
        }

        stage('Yarn Install') {
            steps {
                echo 'Yarn Install'
                echo '******************************'
            }
        }

        stage('Yarn Build') {
            steps {
                echo 'Yarn Build'
                echo '******************************'
            }
        }
        
        stage('Mvn Install') {
            steps {
                echo 'Mvn Install'
                echo '******************************'
            }
        }
        
        stage('Mvn Test') {
            steps {
                echo 'Mvn Test'
                echo '******************************'
            }
        }
        
        stage('Docker Build Image') {
            steps {
                echo 'Docker Build Image'
                echo '******************************'
            }
        }
        
        stage('Docker Push') {
            steps {
                echo 'Docker Push'
                echo '******************************'
            }
        }
        
        stage('Docker Remove Image') {
            steps {
                echo 'Docker Remove Image'
                echo '******************************'
            }
        }

        stage('Deploy') {
            steps{
                echo 'Deploy'
                echo '******************************'
            }
        }
    }
}