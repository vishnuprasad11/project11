pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Get code from a GitHub repository
                git url: 'https://github.com/naiveskill/devops_cred.git', branch: 'main',
                 credentialsId: 'github_creds'
            }
        }
    }
}
