pipeline {
    agent any
    
    stages{
        stage("Code"){
            steps{
                git url: "https://github.com/vedantkuber/DevOps-project.git", branch: "jenkins"
            }
        }
        stage("Build & Test"){
            steps{
                sh "docker build . -t flaskapp"
            }
        }
        stage("Deploy"){
            steps{
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
