pipeline {
    agent {
        docker { image 'nginx:latest' }
    }
    stages {
        stage('setup') {
            steps {
                sh '''
                hadolint Dockerfile
                '''

            }
        }
    }
}