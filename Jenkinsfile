pipeline {
  agent any
  /* environment {
    registry = "impavithra/jenkins"
    registryCredential = 'dockerhub'
    dockerImage = ''
  } */
  stages {
    stage('Cloning Git') {
      steps {
        checkout scm
      }
    }
    stage('Building image') {
      steps {
        sh '''
          docker build --tag "docker-hello-world:latest" .
        '''
      }
    }

# Need to change it to artifactor
  /*  stage('Deploy Image') {
      steps{
        script {
          docker.withRegistry( '', registryCredential ) {
            dockerImage.push()
          }
        }
      }
    } */

 # I feel it is not needed   
   /* stage('Remove Unused docker image') {
      steps{
        sh "docker rmi $registry:$BUILD_NUMBER"
      }
    } */
  }
}
