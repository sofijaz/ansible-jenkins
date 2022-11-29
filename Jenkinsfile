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
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}, git commit is ${env.GIT_COMMIT}"
            }
        }
        stage('Test') {
            steps {
                powershell """
                    if (-not (test-path ${BUILD_INFO}) ) {
                            New-Item ${BUILD_INFO}
                    }
                """

                powershell """
                    echo "QATools version: ${env.GIT_COMMIT}" > ${BUILD_INFO}
                """
            }
        }
    }
}
