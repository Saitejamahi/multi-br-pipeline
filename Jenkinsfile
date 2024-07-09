pipeline {
agent any 
stages {
        stage('WORKDIR')
              {
              steps
                {
                      
                  sh 'pwd'
                sh 'ls'
                  }
               }
            stage(' BUILD')
            {
                steps{
                        sh 'docker build -t login .'
                }
            }
            stage('DEPLOY')
             {
            steps
                {
            sh 'docker container run -dt --name login-con -p 70:80 login'
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
