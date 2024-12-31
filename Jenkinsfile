pipeline {
    agent any
    environment {
        // Define branch-specific environments here if needed
        BRANCH_NAME = "${env.GIT_BRANCH}".replaceFirst('origin/', '')
    }
    triggers {
        // Poll SCM for changes; GitHub webhook triggers it automatically
        pollSCM('* * * * *')
    }
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout([$class: 'GitSCM', 
                        branches: [[name: "*/${BRANCH_NAME}"]],
                        doGenerateSubmoduleConfigurations: false,
                        extensions: [],
                        userRemoteConfigs: [[url: 'https://github.com/harshitsahu2311/Testing']]
                    ])
                }
            }
        }
        stage('Print Branch Name') {
            steps {
                echo "Triggered by branch: ${BRANCH_NAME}"
            }
        }
    }
    post {
        always {
            echo "Pipeline finished for branch: ${BRANCH_NAME}"
        }
    }
}
