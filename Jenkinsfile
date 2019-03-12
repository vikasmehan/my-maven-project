pipeline {

agent any

stages {
	stage('one') {
		steps {
			echo "Hi!! This is step 1"
		}
	}

	stage('two') {
		steps {
			input "Do you want to proceed"
		}
	
	}

	stage('three') {
		steps {
			echo "Hi!! This is step 3"
		}
	
	}

	stage('four') {
		parallel {
			stage('Unit Test') {
				steps {
					echo "Hi!! This is Unit Test stage under stage 4"
				}
			}	
			stage('Integration Test') {
				steps {
					echo "Hi!! This is Integration Test stage under stage 4"
				}	
			}
		}
	}	
}
}
