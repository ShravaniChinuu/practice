#!groovy
properties([pipelineTriggers([upstream('downstream'), githubPush()])])
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
			}
		}
	}
}
