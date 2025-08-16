pipeline {

    agent {label 'First'}

    stages {
        stage ("Git clone") {
            steps {
                git url: 'https://github.com/hashicorp/demo-app-nodejs.git', branch: 'main'
            }
        }

        stage ("Build image") {
            steps {
                sh'''
                docker build -t irady/first_image:latest .
                '''
            }
        }

        stage ("Dockerhub push") {
            steps {
                sh "docker push irady/first_image:latest"
            }
        }

        stage ("Run image") {
            steps {
                sh'''
                docker run -p 8888:8888 first-image
                '''
            }
        }
    }
}