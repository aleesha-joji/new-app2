pipeline {
    agent {
        lable {
            'chrome'
        }
    }
    environment {
        CI = 'true'
        }
    stages {
        stage('Required dependancies') {
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
                sh 'chmod +x ./jenkins/scripts/test.sh'
                sh './jenkins/scripts/test.sh'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}
