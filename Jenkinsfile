pipeline {
    // job in main
    agent any
    stages {
        stage('Print Branch Name') {
            steps {
                echo "Pipeline triggered for branch: ${env.BRANCH_NAME}"
            }
        }
    }
    stage('Checkout') {
            steps {
                script {
                        url: 'https://github.com/harshitsahu2311/Testing', 
                        branch: "${env.BRANCH_NAME}"
                }
            }
        }
}
