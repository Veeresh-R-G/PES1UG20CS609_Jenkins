pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ test.cpp'
        build job: 'PES1UG20CS609-1'
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
    always{
        echo "Pipeline failed ❌"
    }
  }
}
