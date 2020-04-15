pipeline {
  agent any
  stages {
    stage('cloning') {
      steps {
        git(url: 'git@github.com:aftabnaqvi/helloworld.git', branch: 'master', changelog: true, credentialsId: 'jenkens-nuc-key-new', poll: true)
      }
    }

    stage('building') {
      steps {
        sh 'echo "Building the project"'
      }
    }

  }
  environment {
    Test = 'testPipeline'
  }
}
