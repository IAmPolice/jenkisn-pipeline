pipeline {
    agent any
    stages {
        stage ('clone Spring server') {
            steps {
                git 'https://github.com/IAmPolice/spring-servlet.git'
            }
        }
        stage ('clone test') {
            steps {
                git 'https://github.com/IAmPolice/test.git'
            }
        }
        stage('Build') {
            steps {
                sh 'javac HelloWorld.java'
            }
        }
        stage('execute') {
            steps {
                sh 'java HelloWorld'
            }
        }
    }
}