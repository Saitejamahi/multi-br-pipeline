pipeline {
agent any 
stages {
    stage('work dir'){
        steps{
        sh 'pwd'
    }
}
    stage('Build')
    {
        steps
        {
            sh 'docker build -t'
        }
    }
    
    stage('CODE ANALYSIS-SONARQUBE') {
        steps {
           sh 'echo sonar analysis completed'
      }
    }
    stage('BUILD FOR ARTIFACTS') {
        steps {
           sh 'echo build completed'
      }
    }
    stage('BUILD IMAGES-DOCKER') {
        steps {
           sh 'echo docker images build and pushed to docker hub'
      }
    }
  }
}
