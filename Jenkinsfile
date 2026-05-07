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
                /* In this version of the plugin:
                   'name' maps to the Controller Nickname
                   'registry' maps to the Registry Config Name
                */
                neuvector name: 'nvcontroller',
                          registry: 'sec201-registry',
                          repository: 'peteindockerhub/hello-susecon-appco',
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
