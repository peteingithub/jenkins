pipeline {
    agent any
    stages {
        stage('Pre Scan') {
            steps { echo 'Pre Scan commands ...' }
        }
        stage('Image Scan') {
            steps {
                neuvector controllerEndpointUrlSelection: 'nvcontroller',
                          registrySelection: 'sec201-registry',
                          repository: 'peteindockerhub/hello-susecon-appco',
                          tag: 'v0.01',
                          scanLayers: true,
                          numberOfHighSeverityToFail: '10',
                          numberOfMediumSeverityToFail: '100'
            }
        }
        stage('Build') { steps { echo 'Build commands ...' } }
        stage('Deploy') { steps { echo 'Deploy commands ...' } }
    }
}
