pipeline {
    agent any

    tools {
        jdk 'JAVA_HOME'
        maven 'M3'
    }

    stages {

        stage('GIT') {
            steps {
                echo 'Clonage du dépôt...'
                git branch: 'main', 
                    url: 'https://github.com/SelimGharbi10/jenkins-maven-dem.git'
            }
        }

        stage('Build') {
            steps {
                echo ' Compilation du projet...'
                sh 'mvn clean compile'
            }
        }

        stage('Packaging') {
            steps {
                echo ' Génération du package (JAR)...'
                sh 'mvn package'
            }
            post {
                success {
                    echo ' Packaging terminé avec succès !'
                }
            }
        }
    }
}
