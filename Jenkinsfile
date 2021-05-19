pipeline {
	agent { docker { image 'ansible:test' }}
	stages {
		stage('Clone sources') {
			steps{
				git 'https://github.com/CLNRMN/test-repo'
			}
		}
		stage('ansible') {
			steps{
				sh 'ansible -i /var/jenkins_home/workspace/test/Inventory all -m setup'
			}
	}
}
}
