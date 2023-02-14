pipeline {
    agent {
        docker { image 'prom/blackbox-exporter' }
    }
    stages {
        stage ('test') {
            steps {
                sh 'uname -a'
            }
        }
    }
}