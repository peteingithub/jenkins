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
                // The plugin will use the Controller configured in Global System settings by default
                neuvector registrySelection: 'sec201-registry',
                          controller: 'NV_Controller',
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

        stage('Test') {
            steps { echo 'Test commands ...' }
        }

        stage('Release') {
            steps { echo 'Release commands ...' }
        }
    }
}
