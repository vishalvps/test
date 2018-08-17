pipeline {
  agent any
  stages {
    stage('Pre-Build') {
      steps {
        sh '''echo "This Pre-Build Stage"
echo "Building in next stage"'''
      }
    }
    stage('Build') {
      steps {
        sh 'gcc -o hello helloworld.c'
      }
    }
    stage('Post-Build') {
      steps {
        bash hello
        sh 'echo "Build Completed!"'
      }
    }
  }
}
