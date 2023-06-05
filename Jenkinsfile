pipeline {
  agent any
     tools {
    nodejs 'NodeJS' 
  }
  stages {
    stage('Build') {
      steps {
        checkout scm
        sh 'npm install'
      }
    }

//     stage('Test') {
//       steps {
//         sh 'npm test'
//       }
//     }

//     stage('Package') {
//       steps {
//         sh 'npm run build'
//       }
//     }

     stage('Build Docker image'){
           steps {
              
              sh 'docker build -t  raghumugali/docker_jenkins_nodejs:${BUILD_NUMBER} .'
            }
        }
}
}
