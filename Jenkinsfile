pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        sh 'g++ workingg.cpp'
        build job: "PES2UG20CS530-1", wait: true
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
      }
    }
    stage('Deploy'){
      steps{
        sh '/departent/services'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
