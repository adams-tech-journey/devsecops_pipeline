pipeline {
    agent {
        docker { image 'nginx:latest' }
    }
    stages {
        stage('setup') {
            steps {
                sh '''
                ls
                '''
            }
        }
        stage('Front-end') {
            agent {
                docker { image 'n' }
            }
    }
    }
}

pipeline {
    agent none
    stages {
        stage('test1') {
            agent {
                docker { image 'ubuntu:latest' }
            }
            steps {
                sh 'echo hello'
            }
        }
        stage('test2') {
            agent {
                docker { image 'hadolint/hadolint:latest-debian' }
            }
            steps {
                sh 'hadolint Dockerfile'
            }
        }
    }
}
