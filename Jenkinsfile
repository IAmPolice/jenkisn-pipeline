pipeline {
    agent any
    stages {
        stage ('Clone ansible_Spring-Server') {
            steps {
                dir('ansible') {
                    git 'https://github.com/IAmPolice/ansible_spring-servlet.git'
                }
            }
        }
        stage ('Build Spring-Server') {
            steps {
                dir('spring') {
                    git 'https://github.com/IAmPolice/spring-servlet.git'
                }
                sh 'sudo mvn -f spring/ compile package'
                sh 'sudo mv spring/target/spring-servlet-0.0.1-SNAPSHOT.war ansible/re-springServer/files' 
                sh 'ansible-playbook -i ansible/hosts -v ansible/deployment.yml -e vm=local_ubuntu'
            }
        }
    }
}