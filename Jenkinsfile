pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building1..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                echo 'echo "QATools version: ${env.GIT_COMMIT[0..2]}"'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
