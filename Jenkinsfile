pipeline {
    agent any
    stages {
        stage ('clone Spring server') {
            git 'https://github.com/IAmPolice/spring-servlet.git'
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