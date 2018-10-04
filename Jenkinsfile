/********** Declaritive ***********/
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'make'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing ..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'make run'
            }
        }
    }
    post{
        always{
            sh 'make clean'
        }
    }
}

/********** Script ***********/
/*node{
    stage('Build'){
        sh 'make'
    }
    stage('Deploy'){
        sh 'make run'
    }
}*/
