pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS673 PES1UG20CS673.cpp'
                build job: 'PES1UG20CS673-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1111UG20CS673'
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
