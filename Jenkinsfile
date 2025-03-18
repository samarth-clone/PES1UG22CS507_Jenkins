// Write a script containing a Build, Test, and Deploy stage using Groovy. Also
// add a post condition to display ‘pipeline failed’ incase of any errors within
// the pipeline. Refer to attached scripts. Create a new working .cpp file, push it
// to your repository.
// ● For Build stage :- Compile the .cpp file using shell script, build YOUR_SRN- 1.
// ● For the Test stage :- Print output of .cpp file using shell script.
// ● Explore pipeline syntax for references


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
        always {
            echo 'pipeline failed'
        }
    }
}