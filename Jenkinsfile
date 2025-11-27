pipeline {
    agent any
    tools {
        jdk 'JAVA_HOME'
        maven 'M3'
    }
    stages {
        stage('GIT') {
            steps {
                git branch: 'main', 
                    url: 'https://github.com/SelimGharbi10/jenkins-maven-dem.git'
            }
        }
        stage('Compile Stage') {
            steps {
                sh 'mvn clean compile'
            }
        }
    }
}
