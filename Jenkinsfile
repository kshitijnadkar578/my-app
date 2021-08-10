pipeline {
    agent any

    stages {
        stage('clean') {
            steps {
                echo 'clean'
                sh "mvn clean"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "mvn test"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh "mvn package"
            }
        }
    }
}
