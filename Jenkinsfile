node {

	stage ('Apply') {
		dir('dc11-dot-khanh-networking') {
			sh 'terraform apply -auto-approve'
		}		
	}

	stage ('Destroy') {
		dir('dc11-dot-khanh-networking') {
			sh 'terraform destroy -auto-approve'
		}		
	}
}