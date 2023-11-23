pipeline {
    agent any
    stages {
        stage('Deploy') {
            steps {
                sh '''
                kubectl apply -f backend.yaml
                kubectl apply -f frontend.yaml
                sleep 60
                kubectl get services
                '''
            }

        }

    }
}