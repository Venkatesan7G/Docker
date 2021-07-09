pipeline {
  agent {label "linux"}
  option {
	buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
	disableConcurrentBuilds()
  }
  stages {
	stages('hello')
	  steps {
		echo "hello"
		}
	}
  stage('cat Readme') {
	when {
	  branch "Branch1*"
	}
	step {
	  sh '''
		cat Readme.md
		  '''
		}
	}
