pipeline {
    agent any
    stages {
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