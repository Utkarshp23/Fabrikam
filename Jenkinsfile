// Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'node:lts-bullseye-slim' } }
    stages {
        stage('build') {
            steps {
                sh 'node init'
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
