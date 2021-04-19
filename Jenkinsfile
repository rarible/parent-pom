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
        sh 'mvn deploy'
      }
    }
  }
}
