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
       // stage("Deliver") {
       //     steps {
       //         withCredentials([usernamePassword(credentialsId: 'dockerhub', passwordVariable: 'password', usernameVariable: 'username')]) {
       //             sh "docker login -u ${username} -p ${password}"
       //             sh "docker compose push"
       //         }
       //     }
       // }
    }
}