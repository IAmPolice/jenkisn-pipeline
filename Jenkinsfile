pipeline {
    agent any
    stages {
        stage ('Build Spring-Server') {
            steps {
				dir('spring') {
					git 'https://github.com/IAmPolice/spring-servlet.git'
				}
				sh 'mvn compile package'
            }
        }
    }
}