pipeline {

agent any

stages {
	stage('Build') {
		steps {
			echo "Hi!! This is step 1"
		}
	}

	stage('Package') {
		steps {
			input "Do you want to proceed"
		}
	
	}

	stage('Unit Testing') {
		steps {
			echo "Hi!! This is step 3"
		}
	
	}

	stage('Integration Testing') {
		parallel {
			stage('Function Testing') {
				steps {
					echo "Hi!! This is Integration Test stage under stage 4"
				}
			}	
			stage('Deploy') {
				steps {
					echo "Hi!! This is Deploy stage under stage 4"
				}	
			}
		}
	}	
}
}
