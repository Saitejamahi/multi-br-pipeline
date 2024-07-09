pipeline {
agent any 
stages {
    stage('workdir'){
    steps{
            sh 'docker container ls'
        }
    }
    stage('Build')
    {
        steps{
            sh 'docker build -t ecomm .'
        }
    }
    stage('Deploy')
    {
        steps{
            sh 'docker container run -dt --name ecomm-con -p 60:80'
        }
    }
    stage('WORKDIR')
    {
        steps{
            
    
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
