pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/udaykumar987/Home-Construction-Website.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'sudo docker build -t home-construction-app .'
            }
        }

        stage('Stop Old Container') {
            steps {
                sh 'sudo docker stop home-app || true'
                sh 'sudo docker rm home-app || true'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'sudo docker run -d -p 80:80 --name home-app home-construction-app'
            }
        }
    }
}
