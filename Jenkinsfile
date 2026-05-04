pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                git branch: "main",
                    url: "https://github.com/gantay11/sanskargurung_02250368_DSO101_A2.git"
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
        }
        stage("Deploy") {
            steps {
                bat "echo Deployment complete"
            }
        }
    }
}
