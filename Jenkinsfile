pipeline {
  agent any
  stages {
    stage('Stage 1: Running the Pre Build Commands') { 
      steps {
        echo 'E.g. clean up the build system prior to a new build.'
      }
    }
    stage('Stage 2: Build a new Container Image') { 
      steps {
        echo "Build command: \ndockerapp = docker.build('private-registry/app-image:latest', '-f ./src/Dockerfile ./src')"
      }
    }
    stage('Stage 3: Pushing the Image to the Registry') { 
      steps {
        echo "dockerapp.push('latest')"
      }
    }
    stage('Stage 4: Configuring the new App') { 
      steps {
        echo 'Additional commands to update the application configuration ...'
      }
    }
    stage('Stage 5: Scanning the Image with SUSE Security') { 
      steps {
        echo "neuvector nameOfVulnerabilityToExemptOne: '',\nnameOfVulnerabilityToFailOne: '',\nnumberOfHighSeverityToFail: '5',\nnumberOfMediumSeverityToFail: '10',\nregistrySelection: 'private_registry',\nrepository: 'app-image',scanLayers: true,tag: '3.5'"
        //neuvector nameOfVulnerabilityToExemptFour: '',nameOfVulnerabilityToExemptOne: '',nameOfVulnerabilityToExemptThree: '',nameOfVulnerabilityToExemptTwo: '',nameOfVulnerabilityToFailFour: '',nameOfVulnerabilityToFailOne: '',nameOfVulnerabilityToFailThree: '',nameOfVulnerabilityToFailTwo: '',numberOfHighSeverityToFail: '10',numberOfMediumSeverityToFail: '10',registrySelection: 'rmt',repository: "registry.suse.com/bci/bci-base",scanLayers: true,tag: "15.7"
      }
    }
    stage('Stage 6: Deploying the Application to the Develpment Cluster') { 
      steps {
        echo 'kubectl -f new-app-deployment.yaml'
      }
    }
  }
}
