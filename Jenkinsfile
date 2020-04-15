pipeline {
  agent any
  stages {
    stage('cloning') {
      steps {
        git(url: 'git@github.com:aftabnaqvi/helloworld.git', branch: 'master', changelog: true, credentialsId: '20:0a:4e:7d:1e:44:e5:3d:63:55:dd:06:8c:78:90:55', poll: true)
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
