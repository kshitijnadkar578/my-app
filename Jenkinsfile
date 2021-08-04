pipeline {
    agent any

    stages {
        stage('code clone and clean') {
            steps {
                echo 'Git Clone and clean'
                sh "rm -rf my-app"
                sh "git clone https://github.com/kshitijnadkar578/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh "mvn test -f my-app"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh "mvn package -f my-app"
            }
        }
    }
}
