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
				withCredentials([usernamePassword(credentialsId: 'jenkins-rarible-ci', usernameVariable: 'GITHUB_USER', passwordVariable: 'GITHUB_TOKEN')]) {
					sh 'mvn deploy'
				}
      }
    }
  }
}
