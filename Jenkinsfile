pipeline {
    agent any

    stages {
        stage('Handle GitHub Webhook') {
            when {
                expression { currentBuild.rawBuild.getCause('BranchEventCause') }
            }
            steps {
                script {
                    def branchCause = currentBuild.rawBuild.getCause('BranchEventCause')
                    def event = branchCause.getEvent()
                    def deletedBranch = branchCause.getBranch()

                    echo "GitHub Event Type: ${event}"
                    echo "Deleted Branch Name: ${deletedBranch}"

                    // Now you can perform actions based on the event and branch name
                    // For example, trigger specific Jenkins jobs or perform cleanup tasks
                }
            }
        }
    }
}
