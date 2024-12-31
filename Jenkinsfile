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
                script {
   
                    git credentialsId: 'Github-Cred', 
                        url: 'https://github.com/harshitsahu2311/Testing', 
                        branch: "${env.BRANCH_NAME}"
                }
            }
        }
    }
}
