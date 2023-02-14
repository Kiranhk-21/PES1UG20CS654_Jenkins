pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pes1ug20cs654 pes1ug20cs654.cpp'
                build job: 'PES1UG20CS654-1'
            }
        }

        stage('Test') {
            steps {
                sh './PES1UG20CS654'
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
