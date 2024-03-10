pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES2UG21CS247-1'
        sh 'g++ main.cpp -o output'
      }
    }
    stage('Test'){
      steps{
        sh './output'
      }
    }
    stage('Deploy'){
      steps{
       sh 'exit 1'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
  }
}
