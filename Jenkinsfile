pipeline {
    agent any
    stages {
        stage('Cloner le code') {
            steps {
                git credentialsId: 'github-jenkins', url: 'https://github.com/tessnimet/jenkins-pipeline.git', branch: 'main'
            
            }
        }
        stage('Compilation') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage('Tests') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Déploiement') {
            steps {
                echo 'Déploiement terminé !'
            }
        }
    }
}
