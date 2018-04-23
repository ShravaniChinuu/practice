#!groovy


pipeline {
	agent any
parameters {
        booleanParam(defaultValue: true, description: 'Select the box to build or not?', name: 'Build')
	string(defaultValue: '', description: '', name: 'Memory')
	choice(name: 'Nodes',  choices:"Linux\nMac", description: "Choose Node!")
             
	
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
