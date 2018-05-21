pipeline {
  agent {
    docker {
      image 'lilinj2000/dev:centos6.gcc'
    }
  }

  environment {
    home_3rd = '/var/jenkins_home/dist_pkg/3rd/centos6'
    home_libs = '/var/jenkins_home/dist_pkg/libs/centos6'
    home_app = '/var/jenkins_home/dist_pkg/app/centos6'
  }

  stages {
    stage('install') {
      steps {
        sh '''
readerwriterqueue_install_path=${home_3rd}/readerwriterqueue/include
mkdir -p ${readerwriterqueue_install_path}
cp -av *.h ${readerwriterqueue_install_path}
       	'''
      }
    }
  }
  
  post { 
    always { 
      cleanWs()
     }
  }
}
