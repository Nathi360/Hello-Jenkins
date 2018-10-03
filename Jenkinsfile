pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building ..."'
                sh 'make && make run'
                sh 'echo "Build done!"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying ..."'
                sh 'echo "Deploy done!"'
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
            sh 'make clean'
            sh 'echo "Clean-up done!"'
        }
    }
}
