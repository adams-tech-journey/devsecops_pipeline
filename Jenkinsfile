pipeline {
    agent { dockerfile true }
    stages {
        stage('Setup') {
            steps {
                sh'''
                docker run -d -p 80:80 webserver-image:v1         
                curl docker
                '''
            }
        }
    }
}

