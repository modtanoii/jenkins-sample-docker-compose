pipeline {
    agent any
    stages {
        stage('Start container') {
            steps {
                sh 'docker compose up -d --no-color --wait'
                sh 'docker compose ps'
            }
        }
        stage('test access') {
            steps {
                sh 'curl http://localhost:9090'
            }
        }
    }
    post {
        always {
            sh 'docker compose down --remove-orphans -v'
            sh 'docker compose ps'
        }
    }
}