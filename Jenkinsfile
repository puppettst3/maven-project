pipeline {
	/* A Declarative Pipeline */
	agent any

	stages {
		stage('Build') {
			steps {
				sh 'mvn clean package'
			}
		}
		post {
			success {
				echo 'Now Archiving...'
				archiveArtifcacts artifacts: '**/target/*.war'
			}
		}
	}
}
