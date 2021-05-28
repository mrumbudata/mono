pipeline {
agent any
triggers {
    githubPush()
  }
stages {

	

		



		stage('Build and Deploy Branch Development ') {

			   when {
                           branch "testpush"
                       }
	  

				  

				   steps {


				
            sh '''
                echo "mergebranchtestpush7"
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
