pipeline {
agent any

stages {

	

		



		stage('Build and Deploy Branch Development ') {

			   when {
                           branch "testpush"
                       }
	  

				  

				   steps {


				
            sh '''
                echo "mergebranchtestpush8"
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
