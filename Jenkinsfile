#!groovy


pipeline {
	agent any
parameters {
        booleanParam(defaultValue: true, description: '', name: 'userFlag')
    }
	stages {
		stage('Build') {
			steps {
				echo 'Building'
			}
		}
		stage('Test') {
			steps {
				echo 'testing'
		                 echo ' test downstream project'
				 build job: 'downstream'			}
		}
	}
}
