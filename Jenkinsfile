/********** Declaritive ***********/
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building ..."'
                sh 'make'
                sh 'echo "Build done!"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing ..."'
                sh 'echo "Testing done!"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying ..."'
                sh 'make run'
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

/********** Script ***********/
node{
    stage('Build'){
        sh 'make'
    }
    stage('Deploy'){
        sh 'make run'
    }
}
