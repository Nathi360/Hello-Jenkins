pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building ..."'
                sh 'javac *.java'
                sh 'echo "Build done!"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying ..."'
                sh 'java Initiator'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing ..."'
                sh 'echo "Testing done!"'
            }
        }
    }
    post{
        always{
            sh 'rm *.class'
            sh 'echo "Clean-up done!"'
        }
    }
}
