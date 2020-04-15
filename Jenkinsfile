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
        withAnt()
      }
    }

    stage('deploy') {
      steps {
        sh 'echo "deploy to some remote server."'
      }
    }

  }
  environment {
    Test = 'testPipeline'
  }
}