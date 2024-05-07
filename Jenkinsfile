pipeline {
agent any

    triggers {
        pollSCM('* * * * *')
    }

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Patuuuska/JavaSnake'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage"
                sh "docker build -t snake -f ./building/Dockerfile ."
            }
        }

        stage('Test') {
            steps {
                echo "Test stage"
                 sh "docker build -t snake -f ./test/Dockerfile ."
            }
        }

    }
    post{
        success {
            echo 'Success'
        }
        failure {
            echo 'Failed'
        }
    }

}