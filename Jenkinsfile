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
                neuvector scanner: 'NV_Controller',
                          registrySelection: 'sec201-registry',
                          repository: 'peteindockerhub/hello-susecon-appco',
                          tag: 'v0.01',
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
