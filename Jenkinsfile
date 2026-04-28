pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                dir('Task1') {
                    sh 'docker-compose build'
                }
            }
        }

        stage('Deploy') {
            steps {
                dir('Task1') {
                    sh '''
                      docker-compose down || true
                      docker-compose up -d
                    '''
                }
            }
        }
    }
}
