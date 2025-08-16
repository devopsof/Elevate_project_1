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
                docker build -t First-image Dockerfile .
                '''
            }
        }

        stage ("Run image") {
            steps {
                sh'''
                docker run --name First-container First-image
                '''
            }
        }
    }
}