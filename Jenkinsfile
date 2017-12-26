pipeline {
  agent any
  stages {
    stage('install') {
      steps {
        sh '''kernel=`uname -sr | sed --e=\'s/ /\\//\'`

home_3rd=$JENKINS_HOME/3rd/${kernel}

readerwriterqueue_include=${home_3rd}/readerwriterqueue/include

mkdir -p ${readerwriterqueue_include}

cp -av *.h ${readerwriterqueue_include}'''
      }
    }
  }
}