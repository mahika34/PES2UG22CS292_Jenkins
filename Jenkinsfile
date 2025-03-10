pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES2UG22CS292-1'
                sh 'g++ main.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo ' deploy'
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed"
        }
        success {
            echo "Pipeline completed successfully!"
        }
    }
}
