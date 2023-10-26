pipeline {
    agent any

    stages {
        stage('BuildImage') {
            steps {
                sh 'docker build -t myweb1:1 .'
            }
        }
        stage('RunContainer') {
            steps {
                sh 'docker run -d -p 8000:80 myweb1:1'
            }
        }
        stage('verify') {
            steps {
                sh 'docker image ls'
                sh 'docker ps -a'
            }
        }
    }
}
