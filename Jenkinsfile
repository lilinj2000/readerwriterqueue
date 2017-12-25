pipeline {
  agent any
  stages {
    stage('install') {
      steps {
        sh '''kernel=`uname -sr | sed --e=\'s/ /\\//\'`

home_3rd=$JENKINS_HOME/3rd/${kernel}

readerwriterqueue_include=${home_3rd}/readerwriterqueue/include/readerwriterqueue

mkdir -p ${readerwriterqueue_include}

cp -av atomicops.h ${readerwriterqueue_include}
cp -av readerwriterqueue.h ${readerwriterqueue_include}'''
      }
    }
  }
}