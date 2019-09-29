
pipeline {
    agent {
            label 'centos_node'
          } 
    stages {
        stage('clean') { 
            steps {
                    sh 'rm -rf PipelineDemoCode'
                    sh 'git clone https://github.com/lakshmikar23/PipelineDemoCode.git'
                    sh 'mvn clean -f PipelineDemoCode '
            }
        }
        stage('Test') { 
            steps {
                sh 'mvn test -f PipelineDemoCode'
            } 
        }
        stage('Deploy') { 
            steps {
               sh 'mvn package -f PipelineDemoCode' 
            }
        }
    }
}

         
