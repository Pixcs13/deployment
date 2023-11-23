pipeline {
    agent any
    stages {
    //  environment {
    //     MYSQL_ROOT_PASSWORD = credentials("MYSQL_ROOT_PASSWORD")
    // }
    // stages {
    //     stage('Build') {
    //         steps {
    //             sh '''
    //             docker build -t htrvolker/python-backend:letters .
    //             docker build -t htrvolker/python-frontend:red .
    //             '''
    //         }

    //     }
    //     stage('Push') {
    //         steps {
    //             sh '''
    //             docker push htrvolker/python-backend:letters
    //             docker push htrvolker/python-frontend:red
    //             '''
    //         }

    //     }
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