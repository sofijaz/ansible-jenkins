pipeline {
    agent any
    environment {
        BUILD_INFO = "${WORKSPACE}\\buildinfo.txt"
    }
    stages {
        stage('Build') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                echo "QATools version: ${env.GIT_COMMIT}"
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
