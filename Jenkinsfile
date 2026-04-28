pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'docker-compose build'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                  docker-compose down || true
                  docker-compose up -d
                '''
            }
        }
    }
}
