pipeline {
    agent any

    stages {
        stage('Pre Scan') {
            steps {
                echo 'Pre Scan commands ...'
            }
        }

        stage('Image Scan') {
            steps {
                // We removed 'name', 'scanner', 'controller', and 'registry'
                // These are the only parameters your plugin version accepts here
                neuvector repository: 'peteindockerhub/hello-susecon-appco',
                          tag: 'v0.01',
                          scanLayers: true,
                          numberOfHighSeverityToFail: '400',
                          numberOfMediumSeverityToFail: '400'
            }
        }

        stage('Build') {
            steps {
                echo 'Build commands ...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy commands ...'
            }
        }
    }
}
