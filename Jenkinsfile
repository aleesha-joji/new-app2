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
                sh 'ls -ltrh ./jenkins/scripts/'
                sh 'whoami'
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}
