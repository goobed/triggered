pipeline {
    agent any

    environment {
        BRANCH_NAME = "${env.CHANGE_ID}" // The deleted branch name or null if no branch was deleted
    }

    stages {
        stage('Handle Branch Deletion') {
            when {
                expression { BRANCH_NAME != null }
            }
            steps {
                script {
                    echo "Branch '${BRANCH_NAME}' was deleted."
                    
                    // Perform actions based on the deleted branch
                    // For example, trigger specific Jenkins jobs or perform cleanup tasks
                }
            }
        }
    }
}
