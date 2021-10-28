pipeline {
    agent any

    options {
        timestamps()
    }

    stages {
        stage('Build') {
            steps {
                echo "Building.. ${env.BUILD_ID}"
            }
        }
        stage('Test') {
            stages {
                stage('First Test') {
                    steps {
                        echo 'Testing first thing ...'
                    }
                }
                stage('Second Test') {
                    steps {
                        echo 'Testing second thing ...'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
