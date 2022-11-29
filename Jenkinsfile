pipeline {
    agent any
    environment {
        BUILD_INFO = "${WORKSPACE}\\buildinfo.txt"
    }
    stages {
        /*stage('Mkdir') {
            steps {
                powershell """
                        if (-not (test-path ${BUILD_INFO}) ) {
                            New-Item ${BUILD_INFO}
                        }
                """
            }
        }*/
        stage('Build') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Test') {
            steps {
                /*echo "QATools version: ${env.GIT_COMMIT}"*/
                powershell """
                    "QATools version: ${env.GIT_COMMIT}" >> test.txt
                """
            }
        }
    }
}
