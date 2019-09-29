pipeline {
	agent {
              label 'centos_node'
              }
	stages {
		stage('---clean---'){
			steps {
				tool name: 'maven_3.6.1', type: 'maven'
				sh "mvn clean"
			}
		}
		stage('---test---') {
			steps {
				tool name: 'maven_2.2.1', type: 'maven'
				sh "mvn test"
			}
		}
		stage('---package---'){
			steps {
				tool name: 'Maven-3.1.0', type: 'maven'
				sh "mvn package"
			}
		}
	}
}
         