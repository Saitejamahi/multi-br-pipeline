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
            sh 'docker build -t food .'
        }
    }
    stage("DEPLoy')
          {
              steps{
                    sh 'docker container run -dt --name-con -p 90:80 food'
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
