pipeline {
    agent any

    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Build and Run') {
            steps {
                bat 'start /B node index.js'
                sleep 5
            }
        }

        stage('Ping App') {
            steps {
                bat 'curl http://localhost:3000'
            }
        }
    }
}
