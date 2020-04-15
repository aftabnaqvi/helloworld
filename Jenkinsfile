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
        sh '''def antVersion = \'Ant-1.10.7\'
withEnv( ["ANT_HOME=${tool antVersion}"] ) {
    sh \'$ANT_HOME/bin/ant\'
}
'''
      }
    }

  }
  environment {
    Test = 'testPipeline'
  }
}