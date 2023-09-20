pipeline {
    agent any
    options {
        skipDefaultCheckout true
    }

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/nnkhanh/publishRepo'
            }
        }

        stage('Build') {
            steps {
                sh 'terraform validate'
            }
        }
    }
}
