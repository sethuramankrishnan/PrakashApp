pipeline {
    agent any
    stages {
        stage('compile') {
            steps {
	          withMaven(maven : 'maven3.6.2') {
                  sh 'mvn clean compile'
				} 
            }
        }
        stage('test') {
            steps {
	          withMaven(maven : 'maven3.6.2') {
                  sh 'mvn test'
				} 
            }
        }
		stage('deploy') {
            steps {
	          withMaven(maven : 'maven3.6.2') {
                  sh 'mvn deploy'
				} 
            }
        }
            
        
    }
}
