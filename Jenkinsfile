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
                /* controllerEndpointUrlSelection: Maps to your Controller Nickname
                   registrySelection: Maps to your Registry Config Nickname
                */
                neuvector controllerEndpointUrlSelection: 'nvcontroller',
                          registrySelection: 'sec201-registry',
                          repository: 'peteindockerhub/hello-susecon-appco',
                          tag: 'v0.01',
                          scanLayers: true,
                          numberOfHighSeverityToFail: '400',
                          numberOfMediumSeverityToFail: '400',
                          nameOfVulnerabilityToExemptOne: '',
                          nameOfVulnerabilityToExemptTwo: '',
                          nameOfVulnerabilityToExemptThree: '',
                          nameOfVulnerabilityToExemptFour: '',
                          nameOfVulnerabilityToFailOne: '',
                          nameOfVulnerabilityToFailTwo: '',
                          nameOfVulnerabilityToFailThree: '',
                          nameOfVulnerabilityToFailFour: ''
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
