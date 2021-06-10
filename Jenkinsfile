pipeline {
    agent {
        docker {
            image 'node:7-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true'
        }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'pwd'
                sh 'ls'
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
