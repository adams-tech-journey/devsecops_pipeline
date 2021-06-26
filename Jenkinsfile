pipeline {
    agent none
    stages {
        stage('test1') {
            agent { label 'master' }
            steps {
                sh 'echo hello'
            }
        }
        stage('test2') {
            agent {
                docker { image 'hadolint/hadolint:latest-debian' }
            }
            steps {
                sh 'hadolint Dockerfile | tee -a hadolint_lint.txt'
                sh'cat hadolint_lint.txt'
            }
        }
    }
}