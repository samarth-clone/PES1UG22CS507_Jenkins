
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ main/hello.cpp -o hello'
                build 'PES1UG22CS507-1'
            }
        }
        stage('Test') {
            steps {
                sh './hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploying nuke pls take cover if you live in moscow'
            }
        }
    }
    post {
        failure {
            echo 'pipeline failed'
        }
        success {
            echo 'pipeline success'
        }
    }
}