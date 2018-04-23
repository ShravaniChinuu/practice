#!groovy
properties([pipelineTriggers([upstream('upstreamstream'), githubPush()])])
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
