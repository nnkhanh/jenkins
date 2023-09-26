node {

	stage ('Checkout') {
		checkout scmGit(branches: [[name: 'main']],
                userRemoteConfigs: [
                    [ url: 'https://github.com/nnkhanh/publishRepo.git' ]
                ])
	}
	
	/* .. snip ..2 */
	
	stage ('Build') {
		dir('dc11-dot-khanh-networking') {
      			sh 'pwd && ls'
			sh 'terraform init'
			sh 'terraform validate'
		}		
	}

}
