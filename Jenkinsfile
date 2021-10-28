pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Building.. ${env.BUILD_ID}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
