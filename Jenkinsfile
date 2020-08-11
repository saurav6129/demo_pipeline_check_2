pipeline {
	
	agent any
	
	stages {
		
		stage("build") {
			
			when {
				expression{
					env.BRANCH_NAME =='master' 
				}
			}
			
			steps {
				echo 'building the application...'
			
			}
		}
		stage("test") {


			when {
				expression{
					env.BRANCH_NAME =='test'
				} 
			}
			
			steps {
				echo 'testing the application on the test stage...'
				echo 'testing on the test branch'
			}
		}
		
	
		stage("deploy") {
		
			when {
				expression{
					env.BRANCH_NAME =='deploy'
				} 
			}
			
			steps {
				echo 'deploying the application on the final stage ...'
			}
		}
	}

}
