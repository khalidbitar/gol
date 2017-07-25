pipeline {
	agent {
		label "Windows_Slave_01"
	}
	stages {
		stage('build') {
			steps {
				bat 'mvn clean install'
			}
		}
	}
}