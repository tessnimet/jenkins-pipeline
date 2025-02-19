pipeline {
    agent any
    stages {
        stage('Cloner le code') {
            steps {
                git 'https://github.com/TON_REPO/TON_PROJET.git'
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
