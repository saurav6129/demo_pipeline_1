pipeline {
	
	agent any
	parameters {
	
		booleanParam(name: 'executeTest', defaultValue: 'true',description: '')
	
	}
	
	stages {
		
		stage("build") {
			 
			
			 steps {
			 	echo 'building the application...'
			
			 }
		}
		stage("test") {
			when {
				expression {
					params.executeTest
				
				}
			}
				
			steps {
				echo 'testing the application with parameters...'
			 }
		}
		stage("deploy") {
			
			steps {
				echo 'deploying the application...'
			 }
		}
	}

}
