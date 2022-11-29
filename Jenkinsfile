pipeline {
    agent any
    environment {
        BUILD_INFO = "${WORKSPACE}\\buildinfo.txt"
    }
    stages {
        stage('Mkdir') {
            steps {
                powershell """
                        if (-not (test-path ${BINARIES_DIR}) ) {
                            mkdir ${BINARIES_DIR}
                        }
                """
            }
        }
        stage('Build') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                echo "QATools version: ${env.GIT_COMMIT}"
                powershell """
                    "QATools version: ${env.GIT_COMMIT}" >> ${BUILD_INFO}
                """
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
