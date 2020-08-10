pipeline {
	
	agent any
	
	stages {
		
		stage("build") {
			 when {
				 expression{
					BRANCH_NAME =='master' || BRANCH_NAME == 'test'
				}
			
			 steps {
			 	echo 'building the application...'
			
			 }
		 }
		 stage("test") {


			 when {
				 expression{
					BRANCH_NAME =='test'
				} 
			}
			
			steps {
				echo 'testing the application...'
			 }
		 }
		 
		stage("deploy") {
			 when {
				 expression{
					BRANCH_NAME =='master' || BRANCH_NAME == 'test'
				} 
			}
			
			 steps {
				echo 'deploying the application...'
			 }
		 }
	 }

}
