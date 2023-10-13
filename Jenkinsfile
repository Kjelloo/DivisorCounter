pipeline{
    agent any
    triggers {
        pollSCM("* * * * *")
    }
    stages {
        stage("Build") {
            steps {
                sh "docker compose up -d"
            }
        }
        stage("Run") {
            steps {
                sh "docker compose up -d"
            }
        }
    }
}