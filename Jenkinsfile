pipeline {
  agent any
  stages {
    stage('Initial') {
      steps {
        echo 'Check out completed from GIT'
      }
    }
    stage('Build') {
      steps {
        sh '''export JAVA_HOME=/wls_domains/dyesbgot335/jdk1.8.0_221

export JAVA=$JAVA_HOME/bin

export PATH=$JAVA:$PATH

export M2_HOME=/usr/local/apache-maven/apache-maven-3.2.2

export M2=$M2_HOME/bin

export PATH=$M2:$PATH

mvn install dockerfile:build'''
      }
    }
  }
}