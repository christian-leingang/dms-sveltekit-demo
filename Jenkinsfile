pipeline {
  agent any
    
  tools {nodejs "Node 20.0.0"}
    
  stages {
     
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'node test'
      }
    }
  }
}
