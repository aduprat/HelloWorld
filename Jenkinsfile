pipeline {
  agent {
    docker {
      image 'openjdk:11'
    }
  }

  stages {
    stage('Compilation') {
      java HelloWorld.java
    }
  }
}
