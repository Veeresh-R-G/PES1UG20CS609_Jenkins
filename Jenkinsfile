pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ test.cpp'
        echo 'Built Successfully ✅'
      }
    }
    stage('Test') {
      steps {
        sh './a.out'
        echo 'Tested Passed ✅'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed Successfully ✅'
      }
    }
  }
  post{
    failure{
        echo "Pipeline failed ❌"
    }
  }
}
