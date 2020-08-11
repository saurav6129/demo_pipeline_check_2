pipeline {
	
	agent any
	
	stages {
		
		stage("build") {
			
			when {
				expression{
					env.BRANCH_NAME =='master' || env.BRANCH_NAME == 'review'
				}
			}
			
			steps {
				echo 'building the application...'
			
			}
		}
		stage("test") {


			when {
				expression{
					env.BRANCH_NAME =='test'||env.BRANCH_NAME == 'review'
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
					env.BRANCH_NAME =='deploy'||env.BRANCH_NAME == 'review'
				} 
			}
			
			steps {
				echo 'deploying the application on the final stage ...'
			}
		}
		
		stage("review") {
		
			when {
				expression{
					env.BRANCH_NAME =='review'
				} 
			}
			
			steps {
				echo 'reviewing all the stages ...'
			}
		}
	}

}
