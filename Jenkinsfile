pipeline {
agent any
triggers {
    githubPush()
  }
stages {

	

		stage('Static Analysis') {
			  steps{
				 sh '''
					echo "SonarQube Static Analysis goes here"
                
				 '''
			   }
		   }



		stage('Build and Deploy Branch Development ') {

			   when {
                           branch "testpush"
                       }
	  

				  

				   steps {


				
            sh '''
                echo "mergebranchtestpush"
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
