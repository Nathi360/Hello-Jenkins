/********** Declaritive ***********/
pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'make'
                sh 'jar cfe test.jar Initiator *.class'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Testing ..."'
            }
        }
        stage('Deploy') {
            steps {
                sh 'java -jar test.jar'
            }
        }
    }
    post{
        always{
            sh 'make clean'
            sh 'rm -rf test.jar'
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
