pipeline {
    agent any
    tools {
        nodejs "NodeJS"
    }
    stages {
        stage("Checkout") {
            steps {
                git branch: "main",
                    url: "https://github.com/gantay11.git",
                    credentialsId: "github-creds"
            }
        }
        stage("Install") {
            steps {
                bat "npm install"
            }
        }
        stage("Build") {
            steps {
                bat "npm run build"
            }
        }
        stage("Test") {
            steps {
                bat "npm test"
            }
            post {
                always {
                    junit "junit.xml"
                }
            }
        }
        stage("Deploy") {
            steps {
                script {
                    docker.build("02250368/todo-app:latest")
                    docker.withRegistry("https://registry.hub.docker.com", "docker-hub-creds") {
                        docker.image("02250368/todo-app:latest").push()
                    }
                }
            }
        }
    }
}
