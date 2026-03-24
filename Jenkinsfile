pipeline{
	agent none
	stages {
		stage ('parallel stage') {
			parallel{
				stage ('build') {
					agent any
					steps {
						sh 'echo "this is build stage"'
					}
				}
				stage ('deploy') {
					agent { label 'linux' }
					steps {
						sh 'echo "this is deploy stage"'
					}
				}
			}
		}
				stage ('test') {
					agent { label 'cprgm' }
					steps {
					sh 'echo "this is test stage"'
					}
				}
	}
}
