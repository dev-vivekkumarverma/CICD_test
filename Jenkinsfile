pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/dev-vivekkumarverma/Django_dummy_application.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t django_app .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker stop django_app || true'
                    sh 'docker rm django_app || true'
                    sh 'docker run -d --name django_app -p 8000:8000 django_app'
                }
            }
        }
    }
}
