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
                /* scannerSelection: matches the 'Nickname' in Global System Config
                  registrySelection: matches the 'Registry Name' in Global Registry Config
                */
                neuvector scannerSelection: 'NV_Controller',
                          registrySelection: 'sec201-registry',
                          repository: 'peteindockerhub/hello-susecon',
                          tag: '1.0.2',
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
