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
                // controllerEndpointUrlSelection maps to the Nickname 'nvcontroller'
                // registrySelection maps to the Registry Name 'sec201-registry'
                neuvector controllerEndpointUrlSelection: 'nvcontroller',
                          registrySelection: 'sec201-registry',
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

        stage('Test') {
            steps {
                echo 'Test commands ...'
            }
        }

        stage('Release') {
            steps {
                echo 'Release commands ...'
            }
        }
    }
}
