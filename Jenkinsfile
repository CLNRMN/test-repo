pipeline {
	agent { docker { image 'ansible:test' }}
	stages {
		stage('Clone sources') {
			steps{
				git 'https://github.com/CLNRMN/test-repo'
			}
		}
		stage('tst') {
			steps{  
				sh 'id'
			}
		}
		stage('ansible') {
			steps{  
				sh 'ansible localhost -m setup'
			}
		}
}
}
