pipeline {
  agent any
    
  tools {nodejs "Node 20.0.0"}
    
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/christian-leingang/dms-sveltekit-demo.git'
      }
    }
    
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    
    stage('Build') {
      steps {
        sh 'npm run build'
      }
    }  
    
            
    stage('Test') {
      steps {
        sh 'npm run test'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying SvelteKit application"'
        // Add your deployment commands here
      }
    }
  }
}
