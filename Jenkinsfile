pipeline {
    agent any
    triggers {
        pollSCM("* * * * *")
    }
    stages {
        stage("Build") {
            steps {
                script {
                    // Use the correct 'docker-compose' command on Windows
                    def dockerComposeCommand = isUnix() ? 'docker-compose' : 'docker-compose.exe'
                    sh "${dockerComposeCommand} up -d"
                }
            }
        }
        stage("Run") {
            steps {
                script {
                    // Use the correct 'docker-compose' command on Windows
                    def dockerComposeCommand = isUnix() ? 'docker-compose' : 'docker-compose.exe'
                    sh "${dockerComposeCommand} up -d"
                }
            }
        }
    }
}
