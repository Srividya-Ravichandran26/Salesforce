pipeline {
  agent any
  stages {
    stage('Development Build') {
      steps {
        echo 'Pull a code for Dev and Run deployment build'
      }
    }

    stage('QA Build') {
      steps {
        echo 'Run QA Build by pulling git code'
        git(url: 'https://github.com/Srividya-Ravichandran26/Salesforce', branch: 'master', poll: true)
      }
    }

    stage('Certify') {
      steps {
        echo 'Deployment with manual approval'
        input(message: 'Are you sure to certify to deploy the code', ok: 'yes')
      }
    }

  }
}