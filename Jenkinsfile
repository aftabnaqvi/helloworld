pipeline {
  agent any
  stages {
    stage('cloning') {
      steps {
        git(url: 'git@github.com:aftabnaqvi/helloworld.git', branch: 'master', changelog: true, credentialsId: 'f9:cf:0d:15:34:1c:b0:c6:a0:f4:71:80:9f:b1:21:33', poll: true)
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