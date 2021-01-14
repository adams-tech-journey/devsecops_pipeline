pipeline {
    agent { dockerfile true }
    stages {
        stage('Setup') {
            steps {
                sh'''
                docker build .
                docker run -d -p 80:80 
                curl docker
                '''
            }
        }
    }
}