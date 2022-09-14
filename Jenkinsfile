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
        neuvector nameOfVulnerabilityToExemptFour: '',
        nameOfVulnerabilityToExemptOne: '', 
        nameOfVulnerabilityToExemptThree: '', 
        nameOfVulnerabilityToExemptTwo: '', 
        nameOfVulnerabilityToFailFour: '', 
        nameOfVulnerabilityToFailOne: '', 
        nameOfVulnerabilityToFailThree: '', 
        nameOfVulnerabilityToFailTwo: '', 
        numberOfHighSeverityToFail: '400', 
        numberOfMediumSeverityToFail: '400', 
        registrySelection: 'rmt2', 
        repository: "registry.suse.com/bci/bci-base", 
        scanLayers: true, 
        tag: "15.4"
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
