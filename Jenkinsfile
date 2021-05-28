pipeline {
agent any
triggers {
    githubPush()
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



		stage('Build and Deploy Branch Development ') {

			   when {
                           branch "dev"
                       }
	  

				  

				   steps {


				
            sh '''
                echo "mergebranchdev"
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
