node {
	stage ('Checkout') {
	        checkout scm
	}
	
	/* .. snip ..2 */
	
	stage ('Build') {
		sh 'ls -al'
		dir('linux-basic-ssh') {
      			sh 'pwd && ls'
			sh 'terraform init'
			sh 'terraform validate'
		}		
	}

	stage ('Apply') {
		dir('linux-basic-ssh') {
			sh 'terraform apply -auto-approve'
		}		
	}

	stage ('Destroy') {
		dir('linux-basic-ssh') {
			sh 'terraform destroy -auto-approve'
		}		
	}
}
