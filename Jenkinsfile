pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/udaykumar987/Home-Construction-Website.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Stage Completed'
            }
        }

        stage('Deploy to Nginx') {
            steps {
                sh 'sudo cp -r * /var/www/html/'
            }
        }
    }
}
