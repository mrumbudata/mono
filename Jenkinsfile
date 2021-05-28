properties([pipelineTriggers([githubPush()])])

pipeline {
    agent any
    environment {
        CI = 'true'
      
       
    }

    
  stages {

            stage('Unit Test') {
                  steps{
                     sh '''
                        echo "unit test goes here"
                     '''
                   }
               }
       

            stage('Static Analysis') {
                  steps{
                     sh '''
                        echo "SonarQube Static Analysis goes here"
                     '''
                   }
               }
       

       
            stage('Build and Deploy Branch testpush ') {

                       when {
                           branch "testpush"
                       }


                       
                       steps {

                          sh '''
                          echo "branch push13"
                          '''
 
                       }
                 }
   
            stage('Build and Deploy Branch Sanity ') {

                       when {
                           branch "main"
                       }

                       
                       steps {
                           
                          sh '''
                          echo "Branch main"
                          '''
 
                       }
                 }  
            
            stage('Build and Deploy Branch Production ') {

                       when {
                           branch "master"
                       }

                       
                       steps {
                           
                           sh '''
                           echo "Branch Master"
                           '''

                       }
                 }            
         }
post {
        always {
            sh 'echo "Post build stage"'  
        }
        success {
            echo 'I succeeded!'
            
        }
        unstable {
            echo 'I am unstable :('
            
        }
        failure {
            echo 'I failed :(('
            
        }
    }
}