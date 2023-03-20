pipeline {
	agent any
	stages {
		stage('Preparing') {
			steps{
				echo "Pulling... ${env.BRANCH_NAME}"
			}
		}
		stage("Dev"){
			when {
				branch 'dev'
			}
			steps {
				echo 'The pipeline is triggered from Dev branch.'
			}
		}
		stage("Test"){
			when {
				branch 'release'
			}
			steps {
				echo 'The pipeline is triggered from Release branch.'
			}
		}
		stage("Prod"){
			when {
				branch 'main'
			}
			steps {
				echo 'The pipeline is triggered from Main branch.'
			}
		}
	}
}
