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

  }
}