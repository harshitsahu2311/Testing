pipeline {
    agent any
    stages {
        stage('Print Branch Name') {
            steps {
                echo "Pipeline triggered for branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: "${env.BRANCH_NAME}"]],
                    userRemoteConfigs: [[
                        url: 'https://github.com/harshitsahu2311/Testing',
                        credentialsId: 'Github-Cred'
                    ]]
                ])
            }
        }
    }
}
