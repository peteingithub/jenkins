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
                /* Using 'name' to map to the Controller Nickname 
                  and 'registry' to map to the Registry Name.
                */
                neuvector name: 'NV_Controller',
                          registry: 'sec201-registry',
                          repository: 'peteindockerhub/hello-susecon',
                          tag: '1.0.2',
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
