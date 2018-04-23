#!groovy
properties([pipelineTriggers([upstream('upstream'), githubPush()])])
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
		                 #### Testing downstraem project
				 build job: 'downstream'			}
		}
	}
}
