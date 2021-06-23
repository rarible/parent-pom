@Library('shared-library') _

pipeline {
  agent any

	options {
		disableConcurrentBuilds()
	}

  stages {
    stage('install') {
      steps {
        sh 'mvn clean install'
      }
    }
    stage('deploy') {
      steps {
      	deployToMaven('nexus-ci')
      }
    }
  }
}

