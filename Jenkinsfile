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
            parallel {
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
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
                parameters {
                    string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                }
            }
            steps {
                echo 'Deploying....'
                echo "Hello, ${PERSON}, nice to meet you."
            }
        }
    }
}
