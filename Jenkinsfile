// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { 
        docker { 
            image 'node:lts-bullseye-slim'
            args '-p 3000:3000'         
        } 
    }
    tools {nodejs "node"}
    stages {
        stage('build') {
            steps {
//                 sh 'npm init'
                sh 'chown -R 995:993 "/.npm"'
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
