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
                docker build -t first-image .
                '''
            }
        }

        stage ("Run image") {
            steps {
                sh'''
                docker run -p 8888:8888 first-image
                '''
            }
        }

        stage ("Dockerhub push") {
            steps {
                sh "docker push irady/elevate_project_1:tagname"
            }
        }
    }
}