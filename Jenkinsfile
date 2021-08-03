pipeline {
  agent {
    node {
      label 'nodejs-build'
    }

  }
  stages {
    stage('CheckOut-Code') {
      steps {
        git(url: 'https://github.com/avipd/NodeJS-EmptySiteTemplate.git', branch: 'master', changelog: true, credentialsId: 'github', poll: true)
      }
    }

    stage('Install Dependencies {Build}') {
      steps {
        sh 'npm install'
      }
    }

    stage('runing the app') {
      steps {
        sh 'npm start &'
      }
    }

    stage('test the app') {
      steps {
        sh 'curl localhost:8080'
      }
    }

  }
}