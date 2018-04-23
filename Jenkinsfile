#!groovy
properties([parameters([choice(choices: aws\nazure, description: 'this!', name: 'environment'), 
			string(defaultValue: '32000', description: 'please provide meory', name: 'memory', trim: false), 
			booleanParam(defaultValue: false, description: '', name: 'selct defaulst value')])
	   ])

pipeline {
	agent any
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
