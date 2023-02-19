pipeline{
  agent any

  stages{
    stage('Build'){
      steps{
        sh 'g++ temp.cpp -o temp'
        build job: 'PES1UG20CS239-1', wait: false
        echo 'Build by PES1UG20CS239 successful'
      }
    }
    stage('Test'){
      steps{
        sh 'cat temp.cpp'
        echo 'Test by CS239 successful'
      }
    }
    stage('Deploy'){
      steps{
        echo 'Deploy by CS239 successful'
      }
    }
  }
  post{
    failure{
      echo 'Pipeline failed'
    }
  }
}
