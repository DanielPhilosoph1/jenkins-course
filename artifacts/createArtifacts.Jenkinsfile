pipeline {
    agent any
    options {
        copyArtifactPermission 'readArtifact'
    }
    stages {
        stage('Create Artifacts') {
            steps {
                sh "set > report.txt"
            }
        }
    }
    post {
        always {
            archiveArtifacts allowEmptyArchive: true,
            artifacts: 'report.txt',
            fingerprint: true,
            followSymlinks: false,
            onlyIfSuccessful: true
        }
    }
}