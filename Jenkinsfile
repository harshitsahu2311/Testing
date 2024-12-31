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
}
