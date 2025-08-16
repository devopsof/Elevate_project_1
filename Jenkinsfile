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
                docker run --name first-container first-image
                '''
            }
        }
    }
}