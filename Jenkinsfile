pipeline {
  agent any
  stages {
    stage('cloning') {
      steps {
        git(url: 'git@github.com:aftabnaqvi/helloworld.git', branch: 'master', changelog: true, credentialsId: 'jenkins-generated-ssh-key', poll: true)
      }
    }

    stage('building') {
      steps {
        sh '''echo "Building the project"
build.xml'''
      }
    }

  }
  environment {
    Test = 'testPipeline'
  }
}