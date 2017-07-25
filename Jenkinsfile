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
		stage('deploy') {
			steps {
				bat 'sc stop Tomcat7'
				bat 'ping 127.0.0.1 -n 6'
				bat 'xcopy /y "C:\\temp\\CICD Setup\\Jenkins_Slave\\workspace\\GOL_Pipleine\\gameoflife-web\\target\\gameoflife.war" "C:\\temp\\CICD Setup\\tomcat 7\\webapps"'
				bat 'sc start Tomcat7'
			}
		}
	}
}