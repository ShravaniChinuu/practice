#!groovy
properties([parameters([choice(choices: ['aws', 'azure'], description: 'this!', name: 'environment'), string(defaultValue: '32000', description: 'please provide meory', name: 'memory', trim: false), booleanParam(defaultValue: false, description: '', name: 'selct defaulst value')])])
properties([[$class: 'GithubProjectProperty', displayName: '', projectUrlStr: 'https://github.com/ShravaniChinuu/practice.git/'], pipelineTriggers([upstream(threshold: 'UNSTABLE', upstreamProjects: 'upstream'), githubPush()])])
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
