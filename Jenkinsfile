pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS338 PES1UG20CS338.cpp'
                build job: 'PES1UG20CS338-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS338'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Success'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
