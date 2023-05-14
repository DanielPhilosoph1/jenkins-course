pipeline {
    agent any
    
    stages {
        stage('Read Artifacts') {
            steps {
                copyArtifacts projectName: 'createArtifact',
                filter: 'report.txt',
                fingerprintArtifacts: true,
                selector: lastSuccessful()
            }
        }
    }
}