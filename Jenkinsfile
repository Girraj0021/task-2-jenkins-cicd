pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'docker build -t task2-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing the application...'
                sh 'docker run -d --name task2-test -p 8081:80 task2-app'
                sh 'sleep 5'
                sh 'curl -f http://localhost:8081'
            }
        }

        stage('Deploy') {
    steps {
        echo 'Deploying the application...'
        sh 'docker rm -f task2-container || true'
        sh 'docker run -d -p 8082:80 --name task2-container task2-app'
    }
}

    post {
        success {
            echo 'CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'CI/CD Pipeline failed!'
        }
    }
}