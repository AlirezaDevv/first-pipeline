pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/AlirezaDevv/first-pipeline.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Install dependencies (Windows command)
                bat 'npm install'
            }
        }

        // stage('Test') {
        //     steps {
        //         // Run tests (Windows command)
        //         bat 'npm test'
        //     }
        // }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
