pipeline {
    agent {
        docker { image 'nginx:latest' }
    }
    stages {
        stage('setup') {
            steps {
                sh '''
                docker pull hadolint/hadolint:latest-debian
                hadolint Dockerfile

                '''

            }
        }
    }
}