pipeline {
  agent any

  //tools {NodeJS "nodejs"}

  environment {
    NODEJS_HOME = tool 'NodeJS' // Asegúrate de que coincida con el nombre configurado en Jenkins
    CHROME_BIN = "${NODEJS_HOME}/bin/chromium-browser"
    PATH = "${NODEJS_HOME}/bin:${env.PATH}"
    NPM_HOME = "${NODEJS_HOME}/bin"
    //PATH = "${NPM_HOME}:${env.PATH}"
  }

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
