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
        neuvector name: 'NV_Controller', // This MUST match the Nickname in Global System
                  registry: 'sec201-registry', 
                  repository: "peteindockerhub/hello-susecon", 
                  tag: "1.0.2",
                  scanLayers: true, 
                  numberOfHighSeverityToFail: '400', 
                  numberOfMediumSeverityToFail: '400'
      }  
    }
    stage('Image Scan') { 
      steps {
        // We removed scanner: 'NV_Controller'. 
        // Jenkins will use the global default controller automatically.
        neuvector registrySelection: 'sec201-registry', 
                  repository: "peteindockerhub/hello-susecon", 
                  tag: "1.0.2",
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
