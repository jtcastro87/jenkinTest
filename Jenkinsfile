pipeline {
  agent any

  tools {NodeJS "nodejs"}

  stages{

    stage('install'){
      steps{
        sh 'npm install'
      }
    }

    stage('test'){
      steps{
        sh 'npm run test --progress false --watch false'
      }
    }

    stage('Build'){
      steps{
        sh 'npm run build'
      }
    }

    stage('Deploy'){
      steps{
        sh 'mv dist/* /home/joel/miApp'
      }
    }



  }


}
