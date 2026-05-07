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
                // We removed 'controller', 'scanner', and 'name'
                // The plugin will automatically use the Controller defined in Global Settings
                neuvector registrySelection: 'sec201-registry',
                          repository: 'peteindockerhub',
                          tag: '1.0.2',
                          scanLayers: true,
                          numberOfHighSeverityToFail: '400',
                          numberOfMediumSeverityToFail: '400'
            }
        }

        stage('Build') {
            steps { echo 'Build commands ...' }
        }

        stage('Deploy') {
            steps { echo 'Deploy commands ...' }
        }
    }
}
