pipeline {
    agent any

    triggers {
        // This listens for the webhook payload from GitHub
        githubPush() 
    }

    stages {
        stage('Checkout Source Code') {
            steps {
                echo 'Pulling code from the develop branch...'
                // The 'dir' step changes the working directory
                dir('my-source-code') {
                    // 'checkout scm' uses the Git configuration you set up in the Jenkins UI
                    checkout scm 
                }
                echo 'Source code successfully checked out to the my-source-code folder.'
                // Optional: Verify the contents
                sh 'ls -F my-source-code/'
            }
        }
    }
}
