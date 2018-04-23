#!groovy
properties([pipelineTriggers([upstream(threshold: 'UNSTABLE', upstreamProjects: 'upstream'), githubPush()])])
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
