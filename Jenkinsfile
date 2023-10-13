pipeline {
    agent any
    triggers {
        pollSCM("* * * * *")
    }
    stages {
        stage("Build") {
            steps {
                bat 'docker compose build'
            }
        }
        stage("Run") {
            steps {
                bat 'docker compose up -d'
            }
        }
        stage("Deploy") {
            steps {
                withCredentials([usernamePassword(credentialsId: 'dockerhub', passwordVariable: 'password', usernameVariable: 'username')]) {
                    bat 'docker login -u $username -p $password'
                    bat 'docker compose push'
                }
            }
        }
    }
}
