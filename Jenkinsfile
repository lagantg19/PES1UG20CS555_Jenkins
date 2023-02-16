pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output_file working.cpp'
                build job : 'PES1UG20CS555'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './main/output_file'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
