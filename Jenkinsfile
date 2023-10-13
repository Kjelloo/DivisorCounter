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
                script {
                    bat 'docker compose up'
                }
            }
        }
    }
}
