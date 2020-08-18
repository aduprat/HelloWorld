pipeline {
  agent none

  stages {
    stage('Build with several versions') {
      matrix {
        axes {
          axis {
            name 'JDK_VERSION'
            values '11', '12'
          }
        }

        stages {
          stage('Compilation') {
            agent {
              docker {
              image 'openjdk:${JDK_VERSION}'
              }
            }

            steps {
              sh 'java --version'
            }
          }
        }
      }
    }
  }
}
