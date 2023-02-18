// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { 
        docker { 
            image 'node:lts-bullseye-slim'
            args '-p 3000:3000'         
        } 
    }
    stages {
        stage('build') {
            steps {
//                 sh 'npm init'
                sh 'npm install'
            }
        }
        stage('test') {
            steps {
                sh 'node server.js'
            }
        }
    }
}
