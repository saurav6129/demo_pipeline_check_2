pipeline {
	
	agent any
	
	stages {
		
		stage("build") {
			
			when {
				expression{
					env.BRANCH_NAME =='master' || env.BRANCH_NAME == 'test'
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
			}
		}
		
	
		stage("deploy") {
		
			when {
				expression{
					env.BRANCH_NAME =='master'
				} 
			}
			
			steps {
				echo 'deploying the application...'
			}
		}
	}

}
